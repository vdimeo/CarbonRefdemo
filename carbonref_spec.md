# CarbonRef — Product Spec

## 1. Overview

CarbonRef is an early-stage decision cockpit for real estate projects, allowing stakeholders to position a project in terms of cost and carbon relative to:

- a market benchmark
- a target (SIA 390/1, Minergie, etc.)
- their own historical construction practice

CarbonRef is:
- not an LCA tool
- not a database interface

It is a **decision-support interface**, powered by real data but abstracted for usability.

---

## 2. Screens

The demo opens on `Positionnement / Project Intake`.

### 2.1 Positionnement / Project Intake

#### Inputs

- Project type
- Location
- Surface / Volume (SIA)
- Cost estimate
- Target (SIA / Minergie / custom)

#### Default / Sample Values (demo intake form)

| Field | Default value |
|---|---|
| Cost estimate | **850 CHF/m³ SIA** |
| Carbon estimate | 12.5 kgCO₂e/m²/an |
| Surface | 8 000 m² |
| Volume | 28 000 m³ |

Note: default cost must remain within the realistic Swiss market range (800–1000 CHF/m³). Do not use values above 1 200 CHF/m³ as demo defaults.

---

#### User Baseline

Add a new input block before or alongside project inputs:

**"Votre référence habituelle"**

Purpose:
- Capture user's internal baseline (historical ability to build)
- Enable relative positioning vs own practice, not only market

Inputs:
- Reference name (`Nom de la référence`) — e.g. "EMS historique 2022"
- Reference canton (`Canton`) — e.g. "Vaud"
- Reference city (`Ville`) — e.g. "Morges"
- Reference address / note (`Adresse / remarque (optionnel)`) — free text, optional
- Typical cost (CHF/m³ SIA)
- Standard achieved (Minergie, standard légal, etc.)
- Project type (optional)
- Optional qualitative fallback:
  - économique / standard / élevé

Output:
- Display as a point or zone on the chart: **"Référence utilisateur"**

---

#### Graph — Cost vs Carbon

- X-axis: Cost (CHF/m³ SIA)
- Y-axis: Carbon (kgCO₂e/m²/an)

---

#### Carbon Axis Clarification

- Carbon is expressed as **annualized embodied carbon**
- Unit must always display: **kgCO₂e/m²/an**
- Add a visible reference line:
  - **SIA 390/1 target ≈ 9 kgCO₂e/m²/an**

---

#### Displayed Elements

The graph must show:

- Project (current input)
- Market benchmark (aggregated, not explicit comparables)
- Target (SIA / user-defined)
- **User baseline**

---

#### Interpretation Layer

Add a simple interpretation output:

- Gap vs target (carbon)
- Estimated cost impact (CHF/m³)
- Relative position:
  - below / within / above target zone

Message example:

“Votre pratique habituelle vous positionne ici. Pour atteindre la cible SIA, un effort de X kgCO₂e/m²/an est nécessaire, avec un impact estimé de Y CHF/m³.”

---

### 2.2 Leviers

- Identify main drivers of carbon impact
- Show relative contribution of:
  - structure
  - façade
  - systems
  - materials

- Highlight:
  - high-impact decisions
  - low-effort vs high-impact actions

---

### 2.3 Scénarios

- Compare multiple design options
- Show trade-offs:
  - carbon vs cost
  - performance vs feasibility

---

### 2.4 Synthèse

- Provide decision-ready summary
- Include:
  - positioning vs target
  - key actions
  - estimated impact

---

## 3. Data & Metrics

### Carbon Metric

- Primary metric:
  - **kgCO₂e/m²/an**

- Must be consistent with:
  - SIA 390/1 framing
  - early-stage decision usability

- Optional secondary metric (not primary display):
  - total project emissions (tCO₂e)

---

### Cost Metric

- Primary metric:
  - CHF/m³ SIA

---

### Benchmark Data

- Based on real project datasets
- Aggregated and anonymized
- Not exposed directly to users

---

## 4. UX Principles

- Do not expose raw comparables
- Keep interface decision-oriented

- Prioritize **relative positioning over absolute values**
- Anchor user understanding in:
  - their own past performance
  - not only external benchmarks

- Carbon must be:
  - interpretable
  - comparable to a target
  - actionable (linked to effort)

---

## 5. Product Logic

CarbonRef operates in three layers:

1. **Position**
   - Where is the project vs target

2. **Levers**
   - What decisions impact carbon

3. **Evidence (hidden)**
   - Based on real datasets

---

## 6. Key Concepts

- Target (SIA / Minergie / custom)
- Gap vs target
- Trade-off carbon × cost
- Decision-first interface
- Hidden data layer
- **User baseline**

---

## 7. Risks

- Perceived oversimplification
- Confusion with LCA tools
- Misinterpretation of carbon metrics

---

## 8. Opportunities

- Strong demand from asset owners
- Lack of decision-oriented tools
- Ability to leverage existing datasets
- Positioning upstream of LCA workflows
