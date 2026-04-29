# CarbonRef — Product Spec
_Last updated: 2026-04-29 · v0.5 · Owner: Vincent_

## 0. Purpose of this document
Single source of truth for product structure, screens, data model, and interaction
logic. Used as input to AI prompts when iterating on the demo.
Anything not in this doc is out of scope.

## 1. Product framing
One paragraph: what it is, who it's for, the decision it supports.
**In scope (v0.x):** ...
**Out of scope (until vN):** ...

## 2. Screens

The demo opens on `Positionnement / Project Intake`.
Existing modes are shifted after this landing screen:

- 2.1 Positionnement / Project Intake
- 2.2 Decision cockpit
- 2.3 Levers / Pilotage
- 2.4 Lots & coûts
- future: Portfolio / replicate to N parcels

### 2.1 Positionnement / Project Intake

- **Purpose:** point d'entrée par défaut du démo. Permet à l'utilisateur de définir un projet et de le positionner immédiatement sur le nuage de référence cost × carbon.
- **UX intent:** en moins de 2 minutes, l'utilisateur comprend "voici mon projet, voici les actifs comparables, voici où je me situe sur cost × carbon".
- **Entry from:** écran d'ouverture par défaut du démo.
- **Exit to:** §2.2 Decision cockpit (sauvegarde automatique de l'état initial en `V1`).
- **DOM anchor:** `<section id="positionnement">`
- **Components on screen:**
  - formulaire de définition projet
  - logique de filtrage du benchmark
  - graphe benchmark cost × carbon
  - point projet (highlighted)
  - ligne ou zone cible
  - tuiles KPI
  - CTA "continuer vers le cockpit"
- **Project definition fields:**
  - nom du projet
  - type d'actif: residential / office / industrial / healthcare / EMS
  - canton / ville
  - contexte urbain: centre-ville / suburbain / péri-urbain
  - phase: parcel scan / faisabilité / esquisse / pré-projet
  - SRE (m²)
  - surface parcelle (m²)
  - volume estimé (m³)
  - étages hors-sol
  - sous-sols
  - ratio de parking
  - système structurel: béton / bois / hybride / inconnu
  - concept énergétique: CAD / PAC / gaz / inconnu
  - cible: SIA 390/1 / Minergie / personnalisée
- **Benchmark chart:**
  - X axis: coût CHF/m²
  - Y axis: carbone gris kgCO₂e/m²
  - nuage filtré par type d'actif, canton, plage de surface, phase
  - point projet en évidence
  - ligne ou zone cible visible
  - libellés optionnels: "low cost / high carbon", "high cost / low carbon"
- **KPI tiles:**
  - coût estimé CHF/m²
  - carbone gris estimé kgCO₂e/m²
  - écart à la cible (%)
  - percentile dans le benchmark
  - niveau de confiance
- **User actions:**
  - éditer un champ projet → recalcul du point projet et filtrage du nuage
  - changer la cible → mise à jour de la ligne cible et de l'écart
  - cliquer "continuer" → ouvre §2.2 Decision cockpit avec l'état projet courant
  - optionnel: enregistrer l'état initial en `V1`
- **State read:**
  - `benchmarkDataset`
  - `targetLibrary`
- **State written:**
  - `currentProject`
  - `currentVariant`
  - `selectedBenchmarkFilter`

### 2.2 Decision cockpit
- **Purpose:** ...
- **Entry from:** intake screen
- **Exit to:** levers panel, decision stack
- **DOM anchor:** `<section id="cockpit">`
- **Components on screen:** benchmark cloud (PNG), project dot, target line, gap-to-target tile, KPI tiles
- **User actions:** click lever → dot moves; click "save variant" → V_n appended to stack
- **State read:** `currentVariant`, `benchmarkCloud`, `targetLine`
- **State written:** none (read-only view)

### 2.3 Levers panel
... (same shape)

## 3. Data model
```yaml
Project:
  id: string
  name: string
  parcel_id: string?
  canton: enum[VD, GE, ZH, FR, NE, BE, ...]
  city: string?
  urban_context: enum[city_centre, suburban, peri_urban, unknown]
  program: enum[residential, office, industrial, healthcare, ems]
  phase: enum[parcel_scan, feasibility, sketch, pre_project]
  gfa_m2: number
  parcel_area_m2: number?
  volume_m3: number?
  floors_above_ground: integer?
  underground_levels: integer?
  parking_ratio: number?
  structural_system: enum[concrete, timber, hybrid, unknown]
  energy_concept: enum[district_heating, heat_pump, gas, unknown]
  target_id: string
  variants: Variant[]
  
 BenchmarkFilter:
  program: string
  canton: string?
  city: string?
  gfa_range: string?
  phase: string?
  structural_system: string?

BenchmarkPoint:
  id: string
  program: string
  canton: string
  gfa_m2: number
  cost_chf_per_m2: number
  co2_kg_per_m2: number
  source_quality: enum[observed, estimated, synthetic]

Variant:
  id: string         # V1, V2, V3
  parent_id: string?
  levers_applied: LeverApplication[]
  cost_chf_per_m2: number
  co2_kg_per_m2: number
  created_at: datetime
  rationale: string

Lever:
  id: string         # struct_swap_concrete_to_clt
  category: enum[structure, envelope, mep, parking, finishes]
  delta_cost_pct: number
  delta_co2_pct: number
  applicability: string  # plain-English condition
```

## 4. Levers library
Table of every lever with the actual numbers (deltas, conditions, source).
This is the part AI most often gets wrong — keep it explicit.

| id | category | Δ CHF/m² | Δ kg CO2/m² | applicability | source |
|----|----------|----------|-------------|----------------|--------|
| struct_clt | structure | +95 | -180 | bldg ≤ 6 floors | KBOB 2022 |

## 5. Interaction logic
Plain-English event → state-change rules. Example:
- `onLeverToggle(leverId)`: append to `currentVariant.levers_applied`,
  recompute cost & co2 deltas, redraw dot.
- `onSaveVariant()`: deep-clone currentVariant with new id Vn, push to stack.
- `onProjectFieldChange(field, value)`: update `currentProject`, recompute estimated `currentVariant.cost_chf_per_m2` and `currentVariant.co2_kg_per_m2`, update benchmark filter, redraw project dot.
- `onBenchmarkFilterChange()`: filter `benchmarkDataset` by program, canton, size range, phase, and structural system; redraw benchmark cloud.
- `onTargetChange(targetId)`: update `currentProject.target_id`, redraw target line / target zone, recompute gap-to-target.
- `onContinueToCockpit()`: save current state as initial variant `V1`, open Decision Cockpit screen.

## 6. Visual / UX rules
- Language: French primary, English secondary.
- Colors: navy `#0F2A44`, carbon orange `#E8743B`, grey `#6B7280`.
- Typography: Inter, 14/16/24 scale.
- No charts library — d3 + handwritten SVG only (keeps single-file demo).

## 7. Open questions
- [ ] How to handle renovation case toggle? (decide by 2026-05-05)

## 8. Decision log (append-only)
- 2026-04-29 — Inserted §2.1 Positionnement / Project Intake as default landing screen, shifted Levers panel to §2.3. _Why: demo needs a frame-and-position step before any cockpit interaction; aligns with the "in 2 minutes, position your project" pitch._
- 2026-04-29 — Chose single-file HTML over React for demo. _Why: faster iteration, no build step, copy-paste-friendly into prompts._
- 2026-04-22 — Disaggregated cost into struct/env/mep/finishes. _Why: required for lever logic._

## 9. Change log
- v0.5 (2026-04-29) — Added §2.1 Positionnement / Project Intake landing screen; renumbered Levers panel to §2.3.
- v0.4 (2026-04-29) — Added levers library section.
- v0.3 (2026-04-22) — Added disaggregated data model.
