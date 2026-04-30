# CarbonRef — Stratégie technique : du prototype HTML à une app durable

> Document de cadrage. Aucun code ici. Objectif : aligner la roadmap technique sur la maturité produit actuelle (UX journal v8/v9), sans suringénierie.

---

## 0. Diagnostic de départ

Aujourd'hui :

- `index.html` mono-fichier, vanilla JS, SVG dessiné à la main, aucune dépendance runtime.
- État JS en mémoire : `targets`, `project`, `baseline`, `actions`. Réinitialisé à chaque refresh.
- Une seule "instance" de projet vit dans le DOM. Pas de notion de portefeuille.
- Aucun benchmark réel intégré : la zone marché est aujourd'hui une ellipse codée à la main.
- Logique produit **encore mouvante** (cf. UX journal : référence utilisateur, granularité standards, lisibilité du graphe à 4 éléments).

C'est sain pour un prototype. Ça devient bloquant dès que tu veux :
1. Re-démontrer l'app à un client la semaine suivante avec ses données.
2. Capitaliser plusieurs projets de référence chez un même utilisateur.
3. Comparer un projet à un benchmark marché crédible (et pas dessiné à la main).
4. Différencier données privées utilisateur et données partagées.

---

## 1. De quoi as-tu besoin pour passer du démo à une vraie app ?

Trois briques, dans cet ordre :

**a) Persistance** — les données survivent au refresh. Local (navigateur) au début, distant (serveur) plus tard.

**b) Modèle de données structuré** — objets typés (Project, Reference, Benchmark, Target, Scenario, Interpretation), découplés de l'état UI.

**c) Couche d'accès aux données** — un module `store` qui isole le **comment** (localStorage / fichier JSON / API) du **quoi** (les objets métier). Cette couche est le levier le plus important : elle te permet de migrer de palier sans réécrire l'UI.

Tout le reste (auth, multi-utilisateur, sync, dashboard admin) se construit **après**.

---

## 2. Les paliers possibles

| Stage | Stockage | Effort | Quand l'envisager |
|---|---|---|---|
| **1. localStorage** | navigateur de l'utilisateur | ~1–2 j | Maintenant. Démo, prototype, MVP early. |
| **2. Fichiers JSON statiques** | repo Git, lecture seule côté client | ~2–3 j | Pour intégrer le benchmark marché real, séparé du code. |
| **3. Backend léger** | Supabase / Firebase / Node minimal | ~1–2 semaines | Pour multi-utilisateurs, sync entre devices, audit. |
| **4. DB + auth** | Postgres / Supabase + login | ~3–4 semaines | Vraie clientèle, données sensibles, partage par compte. |
| **5. SaaS multi-tenant** | API + workspaces + facturation | ~2–3 mois | Quand tu vends en mode self-serve à plusieurs orgas. |

---

## 3. Pour chaque palier — ce que ça permet, ce que ça ne permet pas

### Stage 1 — `localStorage`

**Permet** : sauvegarde automatique du projet courant, mémorisation de la référence utilisateur, plusieurs projets locaux dans un même navigateur, démo qui survit au refresh.

**Ne permet pas** : aucun partage, aucune sync entre devices/navigateurs, perte totale si l'utilisateur efface son cache.

**Risques** : effacement involontaire, quota navigateur (~5 Mo), pas de versioning.

**Insuffisant quand** : un utilisateur veut accéder à ses projets depuis un autre poste, ou que tu veux mutualiser un benchmark à jour pour tous.

### Stage 2 — Fichiers JSON statiques

**Permet** : intégrer un vrai dataset benchmark (anonymisé, agrégé) versionné dans Git, lu en read-only par le frontend. Découplage clair benchmark / données utilisateur.

**Ne permet pas** : écriture côté serveur, mises à jour en continu sans redeploy, gestion utilisateurs.

**Risques** : si le JSON grossit (>1 Mo) le chargement initial pèse. Le benchmark devient public dès que le fichier est déployé.

**Insuffisant quand** : tu as besoin d'écrire des données partagées, ou de masquer le détail brut du benchmark (LCA confidentielle).

### Stage 3 — Backend léger (Supabase / Firebase)

**Permet** : persistance distante, sync, auth de base, premiers utilisateurs réels, séparation clean privé/partagé.

**Ne permet pas** : logique métier complexe sans Edge Functions, fine-grained access control sans config supplémentaire.

**Risques** : vendor lock-in (modéré), facturation au volume, première dette de sécurité (RLS Supabase à bien configurer).

**Insuffisant quand** : tu as besoin de logique serveur sophistiquée, intégrations avec systèmes existants (ERP, CDE, BIM), ou de garanties on-premise pour clients institutionnels suisses.

### Stage 4 — DB + auth dédiés

**Permet** : contrôle total, hébergement Suisse (atout réglementaire), logique serveur custom, audit trail, RLS fin.

**Ne permet pas** : la simplicité du Stage 3 — tu deviens responsable de l'infra.

**Risques** : coût de maintenance, sécurité, sauvegardes, RGPD/nLPD à assumer.

**Insuffisant quand** : tu veux scaler à >100 organisations clientes avec besoins isolés.

### Stage 5 — SaaS multi-tenant

**Permet** : revenus récurrents, onboarding self-serve, workspaces isolés.

**Risques** : coûts produit énormes si lancé trop tôt (billing, perms, admin, support, RGPD/nLPD à grande échelle).

**Insuffisant quand** : tu attaques l'enterprise sur appel d'offres et besoins d'intégration spécifiques.

---

## 4. Recommandation pour CarbonRef

**Aller en Stage 1 immédiatement, en posant proprement la couche `store`.**

Pourquoi :

- Le produit n'est pas encore stabilisé (UX journal v9, hypothèses ouvertes sur la lisibilité du graphe à 4 éléments). Tout temps investi en backend serait jeté à la prochaine itération.
- localStorage est suffisant pour démontrer à un client, capitaliser une session de travail, et tester la valeur de la "référence utilisateur".
- En posant un module `store` propre dès maintenant, tu pourras passer en Stage 3 plus tard **sans toucher à l'UI**.

À éviter aujourd'hui :

- Backend / DB → prématuré, ralentirait l'itération.
- Framework (React/Vue/Svelte) → coût d'entrée injustifié tant que la logique produit bouge.
- Auth → rien à protéger pour l'instant.

À préparer en parallèle (Stage 2) :

- Externaliser la zone benchmark dans un fichier `benchmarks.json`, ce qui te permet d'y substituer un vrai dataset agrégé (issu de tes 100+ projets) sans toucher au moteur de rendu.

---

## 5. Architecture de données proposée

Décrite en pseudo-objets, sans engagement de syntaxe.

### `Project`
```
id              uuid
name            string
type            enum (logement, EMS, bureau, scolaire, mixte, autre)
canton          string
city            string
gfa             number   // m² SIA
volume          number   // m³ SIA
cost            number   // CHF/m³
co2             number   // kgCO₂e/m²/an
targetId        ref → Target
createdAt       date
updatedAt       date
notes           string
```

### `UserReference` (référence utilisateur / baseline)
```
id              uuid
name            string   // "EMS historique 2022"
canton          string
city            string
addressNote     string   // libre, optionnel
type            enum
typicalCost     number   // CHF/m³
standard        enum (legal, minergie, minergie-P, custom)
qualitative     enum (econ, std, high)   // fallback
notes           string
isPrivate       true     // toujours, par contrat UX
```

### `Benchmark` (donnée mutualisée, lue seulement)
```
id              uuid
segment         { type, canton, system, era }
costRange       [min, p25, p50, p75, max]
co2Range        [min, p25, p50, p75, max]
sampleSize      number
sourceVersion   string
```

→ Jamais individualisé côté UI. Toujours agrégé en zone/ellipse.

### `Target`
```
id              uuid
name            string   // "SIA 390/1", "Minergie", "Cible interne 2030"
co2Limit        number   // kgCO₂e/m²/an
costGuidance    [min, max]   // optionnel
source          enum (sia, minergie, custom)
```

### `Action` / `Lever`
```
id              uuid
rank            int
name            string
sub             string       // sous-titre / scope
hub             string       // grappe (structure, façade, systèmes...)
carbonImpact    [minPct, maxPct]
costImpact      [minPct, maxPct]
confidence      enum (low, med, high)
tag             enum
applied         bool         // état projet, pas action en soi
```

### `Scenario`
```
id              uuid
projectId       ref → Project
name            string       // "Bas carbone", "Référence", "Optimisé coût"
appliedActions  [actionId]
projectedCo2    number
projectedCost   number
breakdownByLot  { gros_oeuvre, second_oeuvre, technique, vrd }
```

### `Interpretation` (calculée, jamais persistée)
```
gapToTarget     number       // kgCO₂e/m²/an
costImpact      number       // CHF/m³
positionLabel   enum (above, within, below)
narrative       string       // texte généré
topActions      [actionId]
```

---

## 6. Distinguer les types de données

| Type | Source | Stockage | Visibilité | Exemple |
|---|---|---|---|---|
| **Privée utilisateur** | saisie | localStorage / DB privée plus tard | jamais sortie | `UserReference`, `Project` |
| **Benchmark partagé** | dataset agrégé | JSON statique / API publique | exposé **agrégé seulement** | `Benchmark`, ellipse marché |
| **Calculée** | dérivée à la volée | RAM uniquement, jamais persistée | UI | `Interpretation`, gap, projection |
| **UI temporaire** | état d'écran | RAM | UI | onglet actif, hover, focus |

Règles dérivées :

- Une donnée privée ne doit jamais traverser la frontière vers le benchmark, même par mégarde (cf. UX journal v9 : "ces données restent privées et internes").
- Une donnée calculée ne doit jamais être stockée — sinon elle se désynchronise. Recalculer toujours.
- Un état UI ne doit jamais finir dans `localStorage` (sauf préférences explicites comme onglet par défaut).

---

## 7. Frontend vs backend

**Reste frontend tant que c'est possible** :

- Saisie projet, référence, baseline.
- Calculs (gap, position, leviers, projection).
- Rendu graphes SVG.
- Persistance locale (Stage 1).

**Bascule backend quand au moins l'un de ces déclencheurs est vrai** :

- Multi-utilisateur réel (plusieurs comptes par organisation).
- Le benchmark devient mutualisé / mis à jour par un admin.
- Besoin d'audit trail (qui a changé quoi, quand).
- Données sensibles (vrais projets de clients institutionnels).
- Intégrations (CDE, ERP, outils LCA externes).

Tant que ces déclencheurs ne sont pas là, le backend serait du poids mort.

---

## 8. Mono-fichier, split, ou framework ?

**Recommandation : garder `index.html` mono-fichier encore 1 à 2 itérations**, jusqu'à validation des hypothèses UX ouvertes (granularité standards, lisibilité du graphe, valeur de la référence utilisateur en test client).

**Splitter en plusieurs fichiers quand** :
- Le JS dépasse ~1500 lignes.
- Tu as 3+ formes de persistance (state UI, projet, références, scenarios).
- Tu commences à avoir des collisions de noms / fonctions globales.

**Migrer vers un framework (React, Svelte, Vue) seulement si** :
- Routing multi-pages réel (ex : `/projects`, `/projects/:id`, `/admin`).
- État partagé devenu trop complexe pour un objet global + `render()`.
- Tu prévois plusieurs "vues" (admin, lecture client, éditeur).

Avant ça, le coût d'entrée du framework dépasserait le bénéfice.

---

## 9. Structure de dossier proposée (à viser pour Phase 2)

```
CarbonRef/
├── index.html                        # markup + structure des écrans
├── assets/
│   ├── css/
│   │   └── style.css                 # variables design + layout
│   └── js/
│       ├── app.js                    # rendu, événements, navigation
│       ├── engine.js                 # calculs métier (gap, agrégation, baseline→carbone)
│       ├── data.js                   # définitions des objets (Project, etc.)
│       ├── store.js                  # adaptateur de persistance (localStorage → API plus tard)
│       └── benchmarks.js             # chargement du dataset benchmark
├── data/
│   ├── benchmarks.json               # benchmark marché agrégé (lu en read-only)
│   ├── targets.json                  # cibles SIA, Minergie, etc.
│   └── actions.json                  # catalogue des leviers
├── docs/
│   ├── carbonref_spec.md
│   ├── carbonref_ux_journal.md
│   ├── architecture_strategy.md      # ce document
│   ├── data_model.md                 # référence canonique du modèle de données
│   ├── backlog_produit.md
│   └── prompt_library.md
└── CLAUDE.md
```

Phase 1 (immédiat) : **n'extrait rien encore**. Garde `index.html` mono-fichier. Crée seulement `docs/architecture_strategy.md` et `docs/data_model.md`.

---

## 10. Workflow Claude Code — l'ordre qui ne casse rien

1. **UX journal** — ajouter une hypothèse explicite (ex : `UX-06 — Persistance locale`) avec la décision et la raison. C'est le palier de réflexion, pas encore d'engagement technique.
2. **Spec** — ajouter une section §9 "Persistance & Modèle de données" qui décrit ce qui est persisté, ce qui ne l'est pas, et pourquoi.
3. **Modèle de données** — créer `docs/data_model.md` avec les objets de la section 5 ci-dessus. Document figé. Toute modif future passe par lui d'abord.
4. **Patcher `index.html`** — introduire un module `store` (toujours dans le même fichier) qui expose `loadProject()`, `saveProject()`, `loadReferences()`, `saveReference(ref)`. L'UI appelle ces fonctions, jamais `localStorage` directement. Modifications **chirurgicales** (cf. règle UX journal §8).
5. **Tester** — recharger la page, vérifier que le projet et la référence utilisateur reviennent.
6. (Plus tard, Phase 2) **Extraire en modules JS** quand le mono-fichier devient inconfortable.

Discipline transverse :
- Toute requête à Claude Code doit citer la section concernée du spec et la règle UX impactée (pratique déjà documentée dans CLAUDE.md).
- Aucune réécriture massive : "modifications chirurgicales uniquement".

---

## 11. Recommandations finales

### Roadmap 3 phases

**Phase 1 — Persistance locale + modèle propre** (1–2 jours)
- Définir les objets dans `docs/data_model.md`.
- Introduire le module `store` (localStorage) dans `index.html`.
- Persister `project`, `userReference`, `actions.applied`.
- Boutons "Nouveau projet" / "Charger projet" / "Réinitialiser".
- Critère de succès : un utilisateur peut quitter et revenir le lendemain et retrouver son projet.

**Phase 2 — Multi-projets + split fichiers + benchmark externe** (~1 semaine)
- Liste de projets utilisateur (chacun un objet `Project` complet, plus juste un seul vivant).
- Référence utilisateur multiple (`UserReference[]`, plusieurs baselines).
- Extraction `app.js` / `engine.js` / `data.js` / `store.js`.
- `benchmarks.json` séparé, lu en read-only ; remplacement de l'ellipse codée en dur.
- Export/import JSON (l'utilisateur peut sauvegarder ses projets en fichier).

**Phase 3 — Backend léger + auth** (2–4 semaines, **uniquement si validé par usage**)
- Choix techno : Supabase recommandé (Postgres + auth + RLS + hébergement EU possible).
- Auth utilisateur basique (email/mot de passe, ou magic link).
- Sync `Project` et `UserReference` privés.
- Benchmark mis à jour côté serveur, lecture publique anonyme acceptable.
- Migration sans douleur car la couche `store` aura déjà été abstraite en Phase 1.

### Le prochain prompt à utiliser pour lancer la Phase 1

> Phase 1 — Persistance locale CarbonRef. Lis d'abord `docs/architecture_strategy.md` (sections 5, 6, 10) et `docs/data_model.md`. Ensuite :
>
> 1. Mets à jour `carbonref_ux_journal.md` en ajoutant `UX-06 — Persistance locale (localStorage)` à la fin du fichier, sans modifier le contenu existant.
> 2. Mets à jour `carbonref_spec.md` en ajoutant `§9 Persistance & Modèle de données` à la fin du fichier, sans modifier le contenu existant.
> 3. Patche `index.html` de manière chirurgicale pour introduire un module interne `store` qui expose `loadProject()`, `saveProject(project)`, `loadUserReference()`, `saveUserReference(ref)`, `clearAll()`. Toutes les écritures vers `localStorage` doivent passer par ce module. Modifie le code existant uniquement aux endroits où il manipule `project` et `baseline`, pour qu'il appelle `store` après chaque mutation. Ajoute les boutons "Nouveau projet" et "Réinitialiser" dans la barre supérieure (sans toucher aux autres éléments).
> 4. Ne touche pas aux écrans Leviers / Scénarios / Synthèse au-delà de l'appel à `store`.
>
> Contraintes : aucune dépendance externe ajoutée, aucune extraction de fichier, aucun changement visuel hors les deux nouveaux boutons.

### Fichiers à créer ou modifier en Phase 1

À créer :
- `docs/architecture_strategy.md` ✅ (ce document)
- `docs/data_model.md` (à rédiger après ce document — référence canonique des objets)

À modifier :
- `carbonref_ux_journal.md` — ajout `UX-06 — Persistance locale` en fin de fichier
- `carbonref_spec.md` — ajout `§9 Persistance & Modèle de données` en fin de fichier
- `index.html` — introduction du module `store`, appels depuis le code existant, deux boutons UI

À ne pas modifier en Phase 1 :
- Les écrans Leviers / Scénarios / Synthèse (au-delà des appels `store`)
- Le rendu graphe Positionnement
- Les couleurs / variables CSS
- Les unités et libellés français

---

## Annexe — Résumé en une phrase

> Tu es en Stage 0. Va en Stage 1 maintenant en posant un module `store` propre, garde le mono-fichier, externalise le benchmark en JSON quand tu auras un vrai dataset, et ne touche au backend que quand tu as un deuxième utilisateur réel à servir.
