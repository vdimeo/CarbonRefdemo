# CarbonRef — UX & Product Journal

## 1. Vision UX

CarbonRef est un cockpit de décision amont permettant aux acteurs immobiliers de situer un projet en termes de coût et de carbone, non pas de manière absolue, mais par rapport à :

- un benchmark marché
- une cible (SIA 390/1, Minergie, etc.)
- leur propre capacité historique à construire

👉 Insight clé (update V8+) :
L’utilisateur ne raisonne pas uniquement en “benchmark externe”, mais d’abord en “référence interne” :
> “Qu’est-ce que je sais déjà faire aujourd’hui, et quel effort cela représente pour atteindre la cible ?”

👉 Conséquence UX :
Le cockpit doit permettre de visualiser simultanément :
- le projet
- le marché
- la cible
- la référence utilisateur

---

## 2. Parcours utilisateur

### Phase 1 — Positionnement

Objectif utilisateur :
- Comprendre où se situe son projet
- Comprendre d’où il part
- Comprendre l’effort à fournir

Questions utilisateur identifiées :

1. Où est mon projet aujourd’hui ?
2. Où suis-je habituellement (mes projets passés) ?
3. Suis-je déjà “bon” ou en retard ?
4. Quel effort reste à faire pour atteindre la cible ?

👉 Évolution UX :

Ajout d’un bloc :
### “Votre référence habituelle”

Permet à l’utilisateur de renseigner :

- coût habituel (CHF/m³ SIA)
- standard atteint (Minergie, standard légal, etc.)
- type de projet comparable
- ou estimation qualitative

👉 Résultat attendu :
Affichage d’un point ou d’une zone “référence interne” sur le graphe coût × carbone

---

## 3. Hypothèses clés

### UX-01 — Référence interne
L’utilisateur se positionne d’abord par rapport à ses projets passés, avant de se comparer au marché

→ Impact produit :
Ajout d’un point “baseline utilisateur” dans le graphe

---

### UX-02 — Unité coût
Le CHF/m³ est une unité plus naturelle que CHF/m² pour la construction

→ Justification :
- correspond aux pratiques entreprises générales
- plus cohérent avec logique volumétrique (structure)

→ Décision :
Remplacer axe coût en CHF/m² → CHF/m³

---

### UX-03 — Lecture carbone
Une valeur carbone seule est peu interprétable

→ Besoin :
Traduire en :
- effort restant
- gap vs cible
- impact projet (tonnes CO₂)

---

### UX-04 — Positionnement relatif
L’utilisateur comprend mieux :
- une position relative (zone)
- qu’une valeur absolue

---

## 4. Décisions prises

- Comparables restent cachés (backend uniquement)
- Interface orientée décision, pas analyse
- Introduction du concept de “gap vs target”
- Introduction du concept de “référence utilisateur”
- Passage CHF/m² → CHF/m³ (à implémenter)

---

## 5. Questions ouvertes

- Les utilisateurs connaissent-ils réellement leur coût en CHF/m³ ?
- Préfèrent-ils :
  - saisir un chiffre précis
  - ou un positionnement qualitatif (économique / standard / premium) ?

- Le point “référence interne” doit-il être :
  - un point précis
  - une zone d’incertitude ?

- Quelle granularité pour les standards ?
  - Minergie
  - Minergie-P
  - Minergie-ECO
  - autres labels ?

- Le graphe devient-il trop complexe avec 4 éléments ?
  (projet / marché / cible / référence utilisateur)

---

## 6. Tests utilisateurs

### Test 1 — Compréhension du graphe

Objectif :
Vérifier si l’utilisateur comprend :
- les axes
- sa position
- l’écart à la cible

---

### Test 2 — Référence utilisateur

Questions à poser :

- “Est-ce que vous savez où vous vous situez habituellement ?”
- “Seriez-vous capable de donner un coût CHF/m³ ?”
- “Est-ce utile de voir votre ‘position habituelle’ ?”

---

### Test 3 — Lecture effort

Objectif :
Tester la compréhension de :

> “Pour atteindre la cible, il faut gagner X kgCO₂/m² et cela implique Y CHF/m³”

---

### Test 4 — Usage en réunion

Contexte :
Comité d’investissement / séance projet

Objectif :
Vérifier si CarbonRef permet :

- de cadrer une discussion
- de challenger un projet
- de décider rapidement

---

## 7. Backlog produit (nouveau)

- [ ] Remplacer CHF/m² → CHF/m³
- [ ] Ajouter bloc “référence utilisateur”
- [ ] Ajouter point/zone “baseline utilisateur” sur graphe
- [ ] Ajouter affichage “effort pour atteindre cible”
- [ ] Tester version simplifiée vs version complète du graphe
