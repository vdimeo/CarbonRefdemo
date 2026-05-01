# Simulation — EMS "Les Hauts du Jorat", Vaud
## Real-world early-stage decision context for CarbonRef product testing

> Project: 84-bed EMS, commune du Jorat (VD)
> MOA: Retraites Populaires (caisse de pensions cantonale)
> Stage: fin esquisse / début APS
> Preliminary LCA result: **11 kgCO₂e/m²·an**
> Date of simulation: début 2026

---

## 1. Project manager mindset

The project manager is **Sébastien M.**, chef de projet immobilier at Retraites Populaires, 12 years in the role, a building engineer (HES) with no formal LCA training. He inherited this dossier 8 months ago when the previous PM moved to the Asset team. The architectural concours SIA 142 was won 18 months ago by a Lausanne agency; the team is now in the final esquisse iteration and starting APS coordination.

### What he knows at this stage
- The **program is locked**: 84 lits long séjour, organised in 6 unités de vie of 14, plus a unité psychogériatrique sécurisée. Surface utile ≈ 4'250 m²; SP SIA 416 ≈ 5'180 m²; volume SIA 416 ≈ 17'600 m³. Plot is 6'400 m², zone d'utilité publique, max R+3 with attique.
- The **cost target is fixed by the DGCS-SASH plafond** under DAEMS: roughly 460 KCHF par lit reconnu pour subventionnement (CFC 1-5, hors terrain, hors équipement médical). Above that, Retraites Populaires absorbs the delta — and the asset committee does not like deltas.
- The **architectural massing**: compact rectangular volume, R+3, single partial basement under half the footprint, attique technique. Ventilated façade option in the concours, but cost engineering may push it to ETICS.
- A **preliminary LCA was just delivered** by the bureau MEP environnemental: 11 kgCO₂e/m²·an, scope SIA 2032 (structure + enveloppe + finitions + technique partielle, amortissement 60 ans). The slide had a green-orange-red traffic light — orange.

### What he doesn't know
- Whether 11 is "good" or "bad" in operational terms. He has no internal benchmark — Retraites Populaires has not built an EMS in 6 years and the previous one was never measured.
- What the 11 is **made of**. The bureau gave a single number, not a hotspot breakdown. He suspects it's mostly béton, but suspects ≠ knows.
- What it would **cost to bring it down to 9** (the SIA 390/1 valeur cible). His instinct says "structure bois — too expensive, acoustic risk, fire derogation, planning delay". He has no quantified figure to back this instinct.
- Whether the **valeur cible is contractual** or just indicative. The cahier des charges of the concours mentioned "Minergie-P-ECO en option, à confirmer en APS" — deliberately vague.
- Whether the **investment committee** in June will ask about carbon, or will only look at CHF/m³. Last year they didn't. This year — uncertain.

### Pressures he faces
- **Budget**: the plafond DAEMS leaves about 6 MCHF of headroom over the architectural ambition. Any structure or façade upgrade eats into that headroom.
- **Timeline**: dépôt permis de construire planned for octobre 2026. Any change after APS (juin 2026) means redoing coordination CVCS — three months minimum.
- **Politics**: the commune has a green executive that publicly committed to "exemplarité carbone" on public buildings. Retraites Populaires has signed the AMAS charte on net-zero by 2050. Both create pressure but neither has translated into a contractual KPI on this dossier.
- **Internal validation**: the asset committee scores projects on IRR, CAPEX, and — newly, since 2025 — a "ESG flag" that is mostly qualitative. Sébastien doesn't know what would trigger a red flag on the ESG dimension.

### How he honestly thinks about cost vs carbon
- Cost is **a hard constraint**: overshoot and the dossier is rejected, his bonus suffers, and the next concours he runs is less ambitious.
- Carbon is **a soft constraint**: overshoot and someone in sustainability writes a memo. The memo is read, filed, and the project proceeds.
- He doesn't disagree with the carbon agenda — he just doesn't have the **language** to argue for it inside his own committee. He needs a way to say "11 means X for our portfolio reporting, going to 9 costs Y, and the trade-off is Z" — in one sentence, with numbers he trusts. Today he has none of that.

---

## 2. Project documents

### A. Project brief — Note de cadrage interne (extrait, p. 1-2)

```
RETRAITES POPULAIRES — DIRECTION IMMOBILIER
NOTE DE CADRAGE — EMS LES HAUTS DU JORAT
Version 4 — 12.03.2026 — S. Massard / O. Petitjean

1. PROGRAMME
   84 lits long séjour (6 UV × 14 lits) + 1 UV psychogériatrie sécurisée (déjà incluse).
   Surfaces de référence (esquisse v3, 02.2026):
     SU (surface utile)                  4'250 m²
     SP (surface de plancher SIA 416)    5'180 m²
     SRE                                 4'880 m²
     Volume SIA 416                      17'600 m³
   Ratio SP/lit reconnu                  61.7 m²/lit  (limite DAEMS: 62)

2. CONTRAINTES
   - Plafond DAEMS investissement reconnu: 460 KCHF/lit (CFC 1-5)
     → Enveloppe reconnue: 38.6 MCHF
     → Enveloppe projet (CFC 1-9): 51.8 MCHF (delta équipement, honoraires, divers)
   - Zone UA, gabarit R+3+att., toit plat exigé par PPA
   - Voisinage classé ISOS: traitement façade soigné requis
   - Permis de construire visé: 10.2026
   - Mise en service: T4 2028

3. OBJECTIFS
   Financiers:
     - CAPEX ≤ 51.8 MCHF (CFC 1-9 hors terrain)
     - CHF/m³ SIA 416 cible: 880 ± 5%
     - DCF/IRR: rendement net cible 3.6% sur 33 ans (plan d'amortissement DAEMS)
   ESG (charte AMAS net-zero 2050):
     - Minergie-P (obligatoire, LVLEne 2024)
     - Minergie-ECO: à étudier en APS (impact ~+1.5% CAPEX selon ratio architecte)
     - Carbone gris: "compatible avec trajectoire AMAS" — non chiffré à ce stade

4. HYPOTHÈSES CLÉS
   - Structure: béton armé conventionnel (dalles 26 cm, voiles porteurs) — option
     bois-béton hybride mentionnée par l'architecte mais non chiffrée
   - Façade: ventilée bois (concours) ou ETICS (option économie)
   - CVC: PAC sol-eau + ventilation double-flux + RCh; pas de gaz
   - Sous-sol: parking 12 places (norme stationnement Jorat: 0.15/lit) +
     locaux techniques + buanderie centralisée; ~1'700 m² hors sol terrassé

5. POINTS OUVERTS
   - Confirmation du choix structure (béton conventionnel vs hybride): décision APS
   - Niveau de label ECO: décision comité immobilier 18.06.2026
   - Stratégie eau chaude sanitaire (volume EMS: ~75 L/lit/jour à 60°C)
```

---

### B. Cost estimate — Estimation à l'esquisse (extrait BAMO)

Source: bureau d'assistance MOA, méthode CFC SIA 416 + ratios par m³ EMS récents (5 références internes Suisse romande, 2021-2024, indexées BFS-IPC 04.2026).

| CFC | Lot | CHF/m³ | Total MCHF | Range |
|---|---|---|---|---|
| 1 | Travaux préparatoires | 22 | 0.39 | ±15% |
| 2 | Bâtiment | 880 | 15.5 | ±8% |
|   ↳ 21 Gros œuvre | | 295 | 5.19 | ±5% |
|   ↳ 22 Enveloppe | | 145 | 2.55 | ±15% |
|   ↳ 23-25 Technique | | 235 | 4.14 | ±10% |
|   ↳ 27-28 Aménagements int. | | 175 | 3.08 | ±10% |
|   ↳ 29 Honoraires | | 30 | 0.53 | ±5% |
| 4 | Aménagements ext. | 18 | 0.32 | ±20% |
| 5 | Frais secondaires | 95 | 1.67 | ±10% |
| **Sous-total CFC 1-5** | | **1'015** | **17.86** | |
| 9 | Équipement médical, mobilier | | 4.20 | ±15% |
| **Total projet** | | | **22.06 MCHF** | |

> *Note: total ci-dessus pour comparaison m³ uniquement. Total global projet incluant terrain, taxes, divers et imprévus = 51.8 MCHF (cf. note de cadrage). L'écart vient principalement de l'équipement médical détaillé, de la TVA, des honoraires complets et de la réserve maître d'ouvrage de 8%.*

**Principaux drivers de coût identifiés:**
1. **Sous-sol et terrassement** (~2.1 MCHF) — sensible au niveau de nappe phréatique (étude géotechnique en cours, risque +0.3 MCHF si rabattement nappe nécessaire).
2. **Structure béton** (~5.2 MCHF) — porte-à-faux du volume nord côté parc impose des sous-poutres importantes; passage en hybride bois-béton supérieur estimé +280 à +450 KCHF (très incertain à l'esquisse).
3. **Façade ventilée bois** (~1.6 MCHF) — alternative ETICS chiffrée à 1.05 MCHF (-550 KCHF) mais perte de valeur architecturale et risque préavis ISOS.
4. **CVC** (~2.8 MCHF) — PAC sol-eau imposée par LVLEne; sondes géothermiques ~85 KCHF par sonde, 8 sondes prévues, sensibilité forte au sol réel.

**Niveau d'incertitude global esquisse: ±10 à ±12% sur le CFC 1-5.**

---

### C. Carbon snapshot — Note bureau environnement (extrait, 1 page)

```
NOTE TECHNIQUE — ÉVALUATION CARBONE PRÉLIMINAIRE
EMS Les Hauts du Jorat — esquisse v3
Bureau XYZ Environnement — 28.02.2026
Méthode: SIA 2032:2020, KBOB 2022, durée d'amortissement 60 ans
Périmètre: structure + enveloppe + finitions + technique de base
            (hors mobilier, hors second œuvre détaillé, hors aménagements ext.)

RÉSULTAT GLOBAL
   11.0 kgCO₂e / m² SRE / an

POSITIONNEMENT
   - SIA 390/1 valeur indicative (Richtwert):     14 kgCO₂e/m²·an  ✓ sous Richtwert
   - SIA 390/1 valeur cible (Zielwert):            9 kgCO₂e/m²·an  ✗ +22%
   - Trajectoire AMAS net-zero 2050 alignée:    ~9-10 kgCO₂e/m²·an

INTERPRÉTATION
   Le projet est conforme aux exigences réglementaires (Richtwert SIA 390/1)
   mais 22% au-dessus de la valeur cible. Cet écart n'est pas critique mais
   nécessitera des choix de conception en APS pour s'aligner sur la
   trajectoire AMAS de Retraites Populaires.

CONTRIBUTEURS PRINCIPAUX (estimation à l'esquisse, à raffiner en APS)
   1. Structure béton (dalles, voiles, fondations)        ~38%   ≈ 4.2
   2. Sous-sol + terrassement (parking + tech.)           ~14%   ≈ 1.5
   3. Façade (variante ventilée bois)                     ~12%   ≈ 1.3
   4. Technique CVCS (PAC, ventilation, distribution)     ~16%   ≈ 1.8
   5. Finitions (chapes, revêtements, cloisons)           ~13%   ≈ 1.4
   6. Toiture                                              ~7%   ≈ 0.8

LEVIERS POTENTIELS À ÉTUDIER EN APS (non chiffrés ici)
   - Réduction épaisseur dalles si concept structurel le permet
   - Béton à teneur CEM III/B (substitution clinker)
   - Hybride bois-béton sur niveaux supérieurs
   - Réduction emprise sous-sol (réétude besoins parking)
   - Façade ETICS vs ventilée: arbitrage carbone défavorable au ventilé bois
     (pondération entretien) — à confirmer

INCERTITUDE
   ±15 à 20% à ce stade. Recalcul prévu en fin APS (06.2026).
```

> Sébastien lit cette note en diagonale. Il retient: *"On est OK réglementaire, on est 22% au-dessus de la cible. Le béton fait 38%. Personne ne me dit ce que ça coûterait de descendre à 9."*

---

### D. Design assumptions — Hypothèses de conception (état esquisse v3)

| Item | Hypothèse | Niveau de fixation | Réversibilité après APS |
|---|---|---|---|
| **Compacité (env/SRE)** | 1.18 (volume compact rectangulaire) | Concours | Faible (impact massing) |
| **Efficience plan (SU/SP)** | 0.82 | APS | Moyenne |
| **Nb niveaux** | R+3+attique | Concours / PPA | Très faible |
| **Sous-sol** | 1 niveau partiel sous moitié emprise | Esquisse | Moyenne (requiert ré-étude programme parking + technique + buanderie) |
| **Structure principale** | Béton armé conventionnel | **Ouverte** — option hybride bois-béton mentionnée mais non chiffrée | Élevée (décision APS) |
| **Trame structurelle** | 7.20 m × 7.50 m, dalles pleines 26 cm | APS | Moyenne |
| **Façade** | Ventilée bois, isolation laine de bois 220 mm | Concours, contestée | Élevée (variante ETICS active) |
| **Toiture** | Toiture plate végétalisée extensive, isolation 200 mm laine roche | Esquisse | Moyenne |
| **Chauffage** | PAC sol-eau, 8 sondes géothermiques | LVLEne — quasi imposée | Très faible |
| **ECS** | Production centralisée + boucle, appoint électrique pic | APS | Moyenne |
| **Ventilation** | Double-flux centralisée par UV | APS | Moyenne |
| **Parking** | 12 places sous-sol (0.15/lit) + 4 places visiteurs ext. | Concours / norme commune | Faible |
| **Label** | Minergie-P (imposé) + ECO en option | Décision comité 06.2026 | Faible si ECO confirmé après cette date |

---

### E. Internal meeting note — Réunion de coordination interne, 14.04.2026

> *Salle de réunion 3.04, Retraites Populaires Lausanne. 14h00–15h20. Compte rendu rédigé par O. Petitjean (BAMO), validé par les participants. Extraits significatifs.*

**Présents:**
- Sébastien M. — chef de projet immobilier (PM)
- Caroline V. — asset manager senior, responsable portefeuille immobilier direct (AM)
- Daniel R. — expert durabilité, équipe ESG groupe (Sust)
- Olivier P. — BAMO, secrétaire de séance

---

> **Sébastien (PM):** "Donc, le bureau env nous a sorti 11. La cible SIA c'est 9. On est à 22% au-dessus. La question pour aujourd'hui: est-ce qu'on s'aligne, ou est-ce qu'on reste là."
>
> **Caroline (AM):** "Avant qu'on parle de s'aligner — c'est combien, 22% au-dessus, en CHF? Parce qu'on a un comité dans 8 semaines et je dois savoir ce que je présente."
>
> **Sébastien:** "On ne sait pas. La note du bureau ne le dit pas. Mon instinct, structure hybride bois-béton, on parle de 300 à 500 KCHF supplémentaires. Mais c'est de l'instinct."
>
> **Caroline:** "500 KCHF c'est 1% du projet. Ce n'est pas mortel. La vraie question c'est si ça nous décale de trois mois sur le permis."
>
> **Daniel (Sust):** "Trois mois je ne pense pas. Ce qui me préoccupe plus: 11 c'est sous le Richtwert, on n'est pas hors-la-loi. Mais sur la trajectoire AMAS — on s'engage à du net-zero 2050 — un EMS livré en 2028 à 11, dans 5 ans on regrettera de ne pas avoir poussé à 9."
>
> **Caroline:** "On regrettera ou on ne regrettera pas?"
>
> **Daniel:** "On regrettera. Tous les projets EMS qu'on lance maintenant, on les exploite jusqu'en 2080. On ne refera pas la structure en 2040."
>
> **Caroline:** "OK. Alors la question c'est: combien coûte le delta 11→9, et qu'est-ce qu'on perd en route. Pas: est-ce qu'on doit le faire."
>
> **Sébastien:** "Sauf que je ne peux pas répondre à la première question proprement à l'esquisse. Ça demande un APS partiel sur deux variantes. C'est 6 à 8 semaines de bureau d'étude supplémentaire."
>
> **Daniel:** "Ou on fait des hypothèses paramétriques. On dit: si on bascule les niveaux 2 et 3 en hybride, on gagne X, on coûte Y. Il y a des bases de données, il y a des projets de référence."
>
> **Sébastien:** "C'est ce qu'on essaie de faire mais on n'a pas l'outil. Le bureau env nous donne un chiffre global, pas une simulation par variante. Et nous, en interne, on n'a pas de cockpit pour ça."
>
> **Caroline:** *(à Daniel)* "Tu peux nous sortir un tableau d'ici 3 semaines? 4 variantes max — base, hybride, ETICS, hybride+ETICS. Trois colonnes: coût delta, carbone delta, risque planning."
>
> **Daniel:** "Je peux essayer mais je vais devoir me baser sur des fourchettes larges. On parlera de ±25% sur les chiffres."
>
> **Caroline:** "C'est OK. Le comité ne veut pas une certitude, il veut un cadre de décision."
>
> **Sébastien:** "Une question bête — le 11, est-ce qu'on est sûr du chiffre? Le bureau env a fait l'esquisse v2 ou v3?"
>
> **Olivier (BAMO):** "v3 mais sans la confirmation de l'épaisseur dalles. Si on passe à 24 cm au lieu de 26, on peut perdre 0.5 sur le chiffre, sans rien changer d'autre."
>
> **Daniel:** "Voilà, exactement le genre de chose qu'on devrait savoir sans demander. C'est notre angle mort."
>
> **Caroline:** "Bon. On acte: 4 variantes, livrables 12.05. Décision en comité 18.06. Sébastien, tu cadres avec le bureau env. Daniel, tu fais le pont méthodo. Je veux une page, pas dix."
>
> **Sébastien:** "Et pour Minergie-ECO?"
>
> **Caroline:** "On en parle quand on aura le tableau. Pas avant."

**Tensions et incompréhensions notées par le BAMO:**
- *PM/AM:* tension classique sur la temporalité de l'incertitude — l'AM accepte l'incertitude si elle est bornée; le PM craint l'engagement sur des chiffres flous.
- *PM/Sust:* le PM ne sait pas distinguer Richtwert et Zielwert — il a entendu "on est OK" et "on est à 22% au-dessus" comme deux messages contradictoires.
- *AM/Sust:* alignement de fond sur la trajectoire long terme; désaccord implicite sur le niveau de preuve attendu en APS.
- *Tous:* l'absence d'un outil partagé pour visualiser le couple coût/carbone par variante crée 30 minutes de discussion qui devraient prendre 5.

---

## 3. Key early-stage decisions

| # | Décision | Impact coût | Impact carbone | Réversibilité |
|---|---|---|---|---|
| 1 | **Compacité du volume** (env/SRE) | ±3-5% CAPEX selon ratio enveloppe | ±10-15% sur poste enveloppe (~1-1.5 kg/m²·an) | **Très faible** — fixée au concours, ne se rejoue qu'en cas d'abandon |
| 2 | **Nombre de niveaux de sous-sol** | -5 à -8% CAPEX si suppression sous-sol | -1.0 à -1.5 kg/m²·an (terrassement + structure SS) | **Faible** — suppression demande ré-étude programme parking, technique, buanderie. Possible jusqu'à fin APS, douloureux après. |
| 3 | **Structure principale (béton vs hybride bois-béton)** | +2 à +5% CAPEX pour hybride sur niveaux 2-3 | -1.5 à -2.5 kg/m²·an | **Élevée à l'esquisse, faible après APS.** Décision typiquement verrouillée à l'APS. Implique compatibilité acoustique (CR EMS norme SIA 181), feu (AEAI), portée. |
| 4 | **Type de béton (CEM I vs CEM III/B avec laitier)** | +0 à +1% CAPEX | -0.5 à -1.0 kg/m²·an | **Élevée jusqu'à l'appel d'offres GO** (DCE). Technique éprouvée, surcoût marginal, planning à vérifier (durcissement plus lent — léger impact phasage hivernal). |
| 5 | **Façade: ventilée bois vs ETICS vs double-peau maçonnée** | -8 à +5% CAPEX selon variante | ±0.8 kg/m²·an (la pondération entretien sur 60 ans inverse l'intuition: l'ETICS est souvent meilleur en carbone gris amorti que le ventilé bois si bardage à remplacer) | **Élevée jusqu'à l'APS** — au-delà, ré-étude détails, étanchéité, préavis ISOS. |
| 6 | **Stratégie ECS** (centralisée + boucle vs décentralisée par UV vs PAC dédiée ECS) | ±1% CAPEX | ±0.4 kg/m²·an (impact distribution + pertes boucle) | **Moyenne** — décidable jusqu'au DCE technique. |
| 7 | **Densification programme** (passage 84 → 90 lits sur même volume = +SU/SP) | -3 à -4% CHF/lit (mais SP/lit baisse en dessous DAEMS) | -0.6 à -0.9 kg/m²·an (effet dilution) | **Très faible** — programme issu d'analyse besoins cantonale, pas négociable. |
| 8 | **Niveau d'isolation enveloppe** (Minergie-P standard vs au-delà) | +0.5 à +1.5% CAPEX | Faible sur carbone gris (matière supplémentaire ~+0.2 kg), mais réduit énergie opérationnelle | **Moyenne** — décision APS, contraint par U-values LVLEne. |
| 9 | **Toiture: végétalisée extensive vs intensive vs PV** | -1 à +2% CAPEX selon mix | ±0.3 kg/m²·an | **Élevée** — décidable jusqu'à fin APS. PV imposé partiellement par LVLEne. |

**Décisions à fort levier carbone et encore réversibles à fin esquisse / début APS:**
3 (structure), 4 (béton bas-carbone), 2 (sous-sol).
**Si Sébastien doit choisir 2 batailles:** structure hybride partielle + CEM III/B sur les éléments massifs. Ce duo seul peut amener le projet de 11 à ~9 sans toucher à l'enveloppe ni au programme.

---

## 4. Decision reasoning walkthrough — Comment Sébastien raisonne

> *Reconstitution honnête du fil de pensée, pas une démarche idéalisée.*

**Étape 1 — Lecture du chiffre.**
Sébastien voit "11 kgCO₂e/m²·an" sur la slide. Premier réflexe: *"C'est quoi 11?"* Il sait qu'il y a un seuil SIA mais ne se souvient pas si c'est 9, 11 ou 14. Il regarde le slide d'à côté: feu orange. *"OK, on est entre."* Il classe l'information comme "à traiter" mais pas urgente.

**Étape 2 — Que faire de ce chiffre.**
Il cherche un point de comparaison interne. Retraites Populaires n'a pas de référence à jour. Il appelle Daniel (sustainability) qui lui répond: *"11 c'est correct mais tu peux mieux."* Réponse non décisionnelle. Sébastien a besoin de quelque chose d'actionnable: combien ça coûte, combien je gagne.

**Étape 3 — Les questions qu'il pose, dans l'ordre.**
1. *Est-ce qu'on est conforme?* → Oui (Richtwert).
2. *Est-ce que le comité va m'embêter avec ça?* → Probablement, depuis la charte AMAS.
3. *Combien ça coûte de passer à 9?* → Personne ne sait précisément.
4. *Est-ce qu'on peut décider ça à l'APS sans ralentir le permis?* → Si on tranche en juin, oui.
5. *Quelle est l'option qui maximise le ratio kgCO₂e économisé / CHF dépensé?* → Question qu'il **devrait** poser mais ne pose pas en ces termes. Il pose à la place: *"on fait quoi de moins cher?"*

**Étape 4 — Ce qu'il décide en pratique.**
- Il **demande au bureau env** un découpage par contributeur (qui aurait dû être livré dès le départ).
- Il **demande à l'architecte** un chiffrage rapide structure hybride niveaux 2-3.
- Il **n'ose pas demander** d'office des variantes ECS/façade par carbone — trop de variables, peur de ralentir l'APS.
- Il **reporte la décision Minergie-ECO** au comité de juin, en espérant que la trajectoire devienne plus claire d'ici là.

**Étape 5 — Là où il se sent aveugle.**
- **Il ne sait pas** si la valeur 11 est robuste (sensibilité aux hypothèses dalles, fenêtres, technique). Il ne sait pas si en raffinant en APS le chiffre va monter ou descendre, ni de combien.
- **Il ne sait pas** quels leviers ont le meilleur rendement coût/carbone. Son intuition (structure bois) est peut-être un leurre — la substitution CEM III/B coûte presque rien et fait économiser 0.5-1 kg.
- **Il ne sait pas** comment positionner ce projet vs les autres EMS qu'il livre dans sa carrière. Il n'a pas de mémoire portfolio. Si le projet d'à côté a fait 13, est-ce qu'il est bon? Si le voisin a fait 8, est-ce qu'il est mauvais? Il navigue sans repère.
- **Il ne sait pas** quoi raconter au comité en une slide. Il devine que "11 vs 9, gap 22%, levier prioritaire structure hybride, coût ~400 KCHF, gain ~2 kg, action: arbitrage en juin" serait la bonne phrase. Il n'a aucun outil qui la lui produit.

---

## 5. Stress-test — Where things actually go wrong

### Bad decisions likely to happen
- **Fausse économie sur la façade.** L'arbitrage ETICS vs ventilée bois sera fait sur le seul critère CAPEX. Personne ne pondère l'entretien sur 60 ans. Le projet bascule en ETICS, "gagne" 550 KCHF, "perd" 0.3 kg/m²·an, et personne ne s'en aperçoit jusqu'à l'audit ESG 2030.
- **Sous-sol non rouvert.** Le programme parking est sous-questionné (12 places pour 84 lits + personnel + visiteurs — très tendu, mais norme commune). Personne ne pose la question de rouvrir la norme avec la commune — pourtant un EMS génère peu de déplacements résidents. Conséquence: on terrasse, on coule, on mange 1.5 kg/m²·an sans débat.
- **CEM III/B oublié.** Le levier le plus rentable carbone/CHF n'est pas dans la conversation à l'APS parce que c'est un sujet "DCE", géré plus tard par l'ingénieur civil seul. Personne ne le remonte au comité. Levier perdu.
- **Choix structure piloté par la peur, pas par les chiffres.** L'hybride bois-béton est rejeté en juin sur l'argument acoustique sans que la note technique acoustique soit vraiment produite. Décision politique habillée en décision technique.

### What is misunderstood
- **Richtwert ≠ Zielwert.** Tous les non-spécialistes (PM, AM, parfois architecte) traitent les deux comme interchangeables. "On est OK" et "on est à 22% de la cible" cohabitent dans la même tête sans dissonance.
- **Le 11 est vu comme une mesure**, pas comme un calcul à hypothèses fortes. Personne ne sait que changer l'épaisseur de dalle de 2 cm bouge le chiffre de 0.5.
- **L'horizon temporel.** L'amortissement carbone est sur 60 ans; les décisions d'APS sont prises sur 4 mois. La fenêtre de décision et la fenêtre d'impact ne sont pas commensurables, et personne ne tente de les rendre commensurables.

### What is ignored
- **Le ratio coût/carbone par levier.** Aucun document ne le calcule. Les leviers sont discutés un par un, jamais classés.
- **Le carbone du sous-sol.** Trop technique, trop tôt, trop déprimant à rouvrir. Rangé comme "fait".
- **L'effet portfolio.** Aucune mémoire institutionnelle: ce projet sera bientôt un comparable, mais pour qui? Pas indexé, pas réutilisé.
- **Le lien LCA → décision.** Le bureau environnement livre un chiffre. Personne ne lui demande une **interprétation actionnable**. Personne ne lui demande de **simuler des variantes**. Le livrable LCA est traité comme un certificat, pas comme un outil.

### What is decided too early
- **Le niveau de sous-sol** (au concours, sans questionnement carbone — c'est une donnée d'entrée pour tout le monde alors que c'est un des plus gros leviers).
- **La compacité** (concours — ce qui est défendable, mais alors il faudrait l'expliciter comme un choix carbone, pas comme un parti architectural).
- **L'absence de Minergie-ECO** (par défaut: si rien n'est tranché, ECO ne se fait pas. Décider de "voir plus tard" = décider de ne pas faire.)

### What is decided too late
- **Le type de béton** — décidé au DCE GO, parfois changé en cours de chantier sur arbitrage planning. À ce moment-là, plus aucun arbitrage carbone n'est possible.
- **La stratégie ECS détaillée** — typiquement APD, alors qu'elle pourrait être cadrée en APS avec un impact carbone clair.

---

## Synthèse pour CarbonRef

Ce que ce projet révèle des besoins du PM, en une page:
1. **Un chiffre de carbone seul ne sert à rien.** Il faut: contexte (cible vs Richtwert), composition (qui contribue), et coût de réduction.
2. **Le PM raisonne en CHF/levier, pas en kg/levier.** L'outil doit traduire le carbone en arbitrage budgétaire, pas demander au PM d'apprendre la sémantique LCA.
3. **Les variantes doivent être paramétriques et instantanées.** Demander 6 semaines à un bureau pour une variante = tuer la décision.
4. **Le sous-sol et le type de béton sont systématiquement sous-discutés.** Un cockpit qui force à poser ces deux questions explicitement aurait un impact disproportionné.
5. **Le PM a besoin d'une phrase à présenter au comité.** "Gap 22%, levier prioritaire X, coût ~Y CHF, gain ~Z kg, décision attendue en juin." Cette phrase est le livrable réel — pas le graphe.
6. **La mémoire portfolio est absente.** Le PM travaille sans repères de ses propres projets passés. La référence "habituelle" du PM est un concept inventé par CarbonRef qui n'existe pas dans son outillage actuel — c'est précisément pour cela qu'elle est utile.
