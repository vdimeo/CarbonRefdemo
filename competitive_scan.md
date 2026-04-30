# CarbonRef — Competitive & Inspiration Scan

*Produced: April 2026 — Senior product strategy perspective*

---

## 1. DIRECT COMPETITORS

### Definition used
Tools that: deal with embodied carbon in construction / operate at project level / include or could extend to a cost dimension.

---

### 1.1 C.Scale (USA) — ⚠️ Closest philosophical twin

**Positioning:** "Whole life carbon platform from concept through construction." Designed as the "shoebox model" of carbon: simple inputs, fast iteration, instant picture of where emissions come from.

**Target users:** Architects, sustainability consultants at concept/schematic stage. Increasingly also developers and investors (post-$2M seed, Nov 2025).

**Strengths:**
- Nails the early-stage philosophy: model in under 10 minutes
- Whole-life carbon (embodied + operational) in one pass
- Free tier (3 projects), low friction entry
- API available — signals a platform ambition
- Recent acquisition of Tally 2.0 → bridging concept stage to BIM-integrated LCA
- Clean, decision-first UX (not a calculation form)

**Weaknesses:**
- **No cost dimension** — carbon only, no CHF/m³ equivalent
- **No user baseline** — compares to benchmark, not to user's own history
- **US-centric** — benchmarks, regulation framing, units (imperial)
- **No Swiss / SIA 390/1 alignment** whatsoever
- Still primarily a carbon tool, not a decision cockpit for non-experts
- Requires some sustainability literacy to interpret outputs

**Is it a real competitor to CarbonRef?**
Philosophical cousin, not a current competitor. C.Scale is for architects and consultants in North America. CarbonRef targets Swiss MOA (maîtres d'ouvrage) and investment committees. The cost-carbon trade-off axis, the SIA 390/1 anchor, and the "user baseline" concept are CarbonRef-specific and absent from C.Scale. *However: if C.Scale expands to Europe and adds a cost axis, the overlap becomes real.*

---

### 1.2 Preoptima CONCEPT (UK) — ⚠️ Technically closest, wrong audience

**Positioning:** "Real-time whole-life carbon assessments and carbon optioneering from earliest design stages." Backed by Nemetschek Group (investment 2023), Innovate UK grant for PACER (local authority planning applications).

**Target users:** Architects and structural engineers at schematic stage. Explicitly claims "no LCA expertise required" — but the UX still assumes technical literacy.

**Strengths:**
- Patented AI for automated material quantity take-offs from massings
- Instant feedback on carbon hotspots — fast iteration
- Custom baselines and target-setting at project level
- Whole-life (embodied + operational) with structural equation modeling
- Strong academic backing (10+ years of research)
- Backed by Nemetschek — distribution potential is serious

**Weaknesses:**
- Still functionally an LCA tool with simplified inputs — not a decision cockpit
- **No cost-carbon trade-off** — cost is not in the UX
- **No user baseline** (historical comparison to own practice)
- UK/Europe framing but no SIA / Swiss market focus
- Non-expert users (MOA, investment committee) are not the actual ICP

**Is it a real competitor to CarbonRef?**
Significant technical overlap at concept stage, but completely different target user and missing the cost dimension. Preoptima serves architects who need to justify carbon choices. CarbonRef serves investors who need to make project decisions. The audiences are adjacent but the decision context is different. *Risk: Preoptima could reframe its positioning toward decision-makers if it adds a cost axis.*

---

### 1.3 One Click LCA — Early Design Module (Finland/Global) — Not a real competitor

**Positioning:** Global leader in building LCA. Added an "Early Design Decarbonization" module to address early-stage use cases (also offers "Planetary" as a free benchmarking entry point).

**Target users:** LCA specialists, sustainability teams, architects. Not MOA.

**Strengths:**
- Enormous database (EPDs, materials), global coverage
- Brand authority in the LCA space
- Planetary (free) lowers the barrier to entry
- European embodied carbon benchmarks published

**Weaknesses:**
- LCA tool with early-stage mode — not a decision cockpit
- Complexity is intrinsic: the product logic is bottom-up (materials → building), not top-down (project → positioning)
- No cost-carbon positioning
- No Swiss-specific SIA 390/1 framing
- Not designed for non-specialists

**Is it a real competitor to CarbonRef?**
No. Different layer of the value chain. One Click LCA is what happens *after* someone like CarbonRef has oriented the decision. The risk is confusion in the market — buyers might conflate them.

---

### 1.4 SIA 390/1 Calculation Aid (Switzerland) — Not a competitor, but shapes expectations

**Positioning:** Free official tool from SIA for greenhouse gas accounting of buildings per SIA 390/1, covering preliminary project phase.

**Target users:** Engineers, planners, compliance officers. Explicitly a calculation tool.

**Strengths:**
- Free, authoritative, aligned with Swiss regulation
- Accepted for compliance submission

**Weaknesses:**
- Spreadsheet logic (not a UX product)
- No cost dimension
- No decision orientation — produces numbers, not positions
- Not usable by non-specialists
- Requires knowing what to input (KBOB material types, quantities)

**Is it a real competitor to CarbonRef?**
No — but it is the *default fallback* for Swiss engineers. CarbonRef's value prop needs to clearly explain why it exists *alongside* (upstream of) this tool, not against it.

---

### 1.5 Ecotool / Lesosai / Enerweb (Switzerland) — Calculation tools, not competitors

These are Swiss tools for early or detailed phase LCA, as referenced in SIA documentation. They are engineering calculation environments, not decision interfaces. No cost axis. No decision orientation.

**Verdict:** Instruments for specialists. CarbonRef explicitly lives upstream and above these.

---

## 2. INDIRECT COMPETITORS

*More important than direct competitors — these define the decision-making UX that CarbonRef must beat.*

---

### 2.1 CRREM — Carbon Risk Real Estate Monitor (Global, free)

**What it does:** Operational decarbonization pathways for standing assets and portfolios. Tells you the "stranding year" — when a building's carbon intensity crosses the Paris-aligned pathway and becomes a stranded asset.

**Decision problem it solves:** When does my building become un-investable? How does my portfolio compare to science-based targets?

**Why it's relevant to CarbonRef:**
- Same user (asset owner, investment committee)
- Same logic: position vs target, gap vs benchmark
- "Stranding year" is a brilliant UX move — one number, maximum decision gravity
- But: operational carbon (in-use energy), not embodied. Existing buildings, not new projects.

**What CarbonRef can learn:**
→ The "stranding year" concept. A single, high-stakes number that frames urgency. CarbonRef should think about its equivalent: not just "gap vs target" but *what does this gap cost or risk over time?*
→ CRREM's pathway visualization (project carbon vs declining threshold over time) is excellent for non-experts.

---

### 2.2 TestFit (USA) — Site Feasibility Parametric Tool

**What it does:** Parametric building massing and site solver. Input: site, program, unit mix, cost targets. Output: optimized massing with instant density/cost/feasibility readout.

**Decision problem it solves:** What can I build on this site, how dense, at what cost?

**Why it's relevant to CarbonRef:**
- Defines the gold standard for early-stage, non-expert decision support
- Instant solve, no waiting — the UX respects that decision meetings move fast
- All key indicators on one screen: no tab navigation for core insight
- Free (as of 2025) — deliberately disrupted the market by lowering friction

**What CarbonRef can learn:**
→ Single-screen, instant feedback philosophy. If CarbonRef requires 4 tabs to understand the situation, it's too slow for a committee meeting.
→ "One optimal answer" approach — not a range of options requiring expertise to interpret.
→ The willingness to give a *recommendation*, not just a visualization.

---

### 2.3 Autodesk Forma (formerly Spacemaker) — Environmental Early Design

**What it does:** Early-stage environmental analysis (wind, noise, sunlight, daylight, operational energy). Cloud-based, integrates with Revit.

**Decision problem it solves:** How does site placement, massing, and orientation affect environmental performance?

**Why it's relevant to CarbonRef:**
- Pioneered "environmental analysis at massing stage" — normalized the idea that sustainability metrics belong at concept
- Strong visualization: instant heatmaps, not tables
- Recently added embodied carbon analysis (April 2024 release)

**What CarbonRef can learn:**
→ The heatmap / visual positioning approach: understanding a position spatially is faster than reading a number.
→ Normalization: Spacemaker/Forma proved you can put complex sustainability metrics in front of non-LCA users if the UX is right.

---

### 2.4 Feasibility.pro / Feasibly / Archistar — Financial Feasibility Tools

**What they do:** Develop-to-sell/hold financial feasibility modeling. Inputs: land cost, construction cost, GFA, revenue assumptions. Output: IRR, equity return, feasibility verdict.

**Decision problem they solve:** Is this project financially viable?

**Why it's relevant to CarbonRef:**
- Same early-stage moment, same non-expert audience
- Proven that developers/MOA will input into a simplified tool if the output is decision-ready
- "Green / red / amber" verdict pattern is standard
- Feasibly explicitly targets investment committee presentation

**What CarbonRef can learn:**
→ The "verdict" pattern: not just positioning, but a clear go/no-go or "effort required" judgment.
→ The importance of a single exportable output (PDF/slide) — decisions made in meetings, not in tools.
→ Archistar uses satellite + planning data to reduce input friction — CarbonRef could pre-populate canton-level benchmarks.

---

### 2.5 GRESB (Global) — ESG Benchmarking for Real Estate Portfolios

**What it does:** Annual ESG assessment and benchmarking for real estate funds and assets. Produces a GRESB Score and peer comparison.

**Decision problem it solves:** How does my fund compare to peers on ESG? What is the narrative for investors?

**Why it's relevant to CarbonRef:**
- Same C-suite / investment committee audience
- "Position vs peer group" is the core output, not raw metrics
- GRESB score is meaningless in isolation — its power is relative positioning
- Deeply embedded in LP due diligence and capital allocation decisions

**What CarbonRef can learn:**
→ The score as narrative: "you're in the top quartile" is more powerful than any raw number.
→ Peer comparison as the core value proposition, not accuracy.
→ The annual cycle creates a recurring engagement mechanism — CarbonRef could think about project lifecycle hooks.

---

### 2.6 REMMS (Switzerland) — Operational Sustainability Rating

**What it does:** Real Estate Meta-rating & Monitoring on Sustainability. Multi-criteria sustainability rating for Swiss properties. Free for small owners.

**Decision problem it solves:** What is the overall sustainability profile of my asset?

**Why it's relevant:**
- Swiss-specific, same MOA user base
- Rating logic (aggregate → position) not calculation logic
- Free positioning as an adoption strategy

**What CarbonRef can learn:**
→ Free entry for small owners is a land-and-expand strategy in Swiss real estate. CarbonRef could consider a freemium tier.
→ "Meta-rating" approach: aggregate complexity into a single score — reduces cognitive load for non-experts.

---

## 3. UX / PRODUCT INSPIRATION

*Any industry. The question is: how do great products handle uncertainty, positioning, and non-expert decision support?*

---

### 3.1 CRREM "Stranding Year" — One Number, Maximum Decision Weight

**What they do:** Turn a complex decarbonization pathway analysis into a single year when the asset becomes stranded.

**What makes the UX strong:**
- Radical simplification: 40 years of carbon trajectory compressed into one date
- Immediate decision relevance: "2031" creates urgency that "14 kgCO₂/m²/yr" does not
- The pathway graph (asset line vs benchmark curve) makes the gap visually obvious

**What CarbonRef can reuse:**
→ Define CarbonRef's equivalent of the "stranding year" — a single synthesized metric with decision weight. Not "gap = 3.5 kgCO₂/m²/an" but something like "this project requires a +8% cost effort to be SIA-compliant."

---

### 3.2 TestFit — Instant Solve, No Waiting

**What they do:** Parametric massing that solves in real time as you adjust sliders.

**What makes the UX strong:**
- Zero latency between input and output — the chart changes as you type
- The result is *one* optimized answer, not a menu of options requiring expertise
- Clean differentiation between "what you can change" (left panel) and "what it means" (right panel)

**What CarbonRef can reuse:**
→ CarbonRef already does this (render() on every input) — reinforce it. Make the reactive update feel fast and "alive." Every input change should produce visible movement in the chart.
→ The left/right split (inputs | outputs) is a proven pattern for decision tools.

---

### 3.3 Stripe Dashboard — KPI Positioning with Trend Direction

**What they do:** Financial dashboard for operators. Revenue, disputes, payouts — each with trend direction vs prior period.

**What makes the UX strong:**
- Every number has a direction (↑↓) and a benchmark (vs period, vs target)
- The "position" matters more than the absolute value
- Color coding is minimal and semantic: green isn't "good," it means "up"

**What CarbonRef can reuse:**
→ In the Synthèse tab: each KPI should have a position indicator (above / within / below target zone), not just a number. The arrow + color pattern reduces cognitive load for non-experts.
→ Avoid color as decoration. Use it only for semantic meaning (red = above target, green = below).

---

### 3.4 Linear (Project Management) — Density without Clutter

**What they do:** Engineering project management. All issues, projects, cycles visible without switching context.

**What makes the UX strong:**
- Extremely dense information, but never feels cluttered — achieved by whitespace discipline and typographic hierarchy
- Everything keyboard-accessible — respects that power users move fast
- The "triage" mindset: every item has a status that implies a next action

**What CarbonRef can reuse:**
→ The "Leviers" tab should feel like Linear's issue list: ranked, each with a status, each implying an action. Not a menu of options — a prioritized list.
→ Whitespace discipline: CarbonRef's current risk is information overload on the Positionnement chart. Follow Linear's lead: show only what's actionable, hide what's context.

---

### 3.5 Figma FigJam — Low-Friction Entry, High Perceived Value

**What they do:** Collaborative whiteboard. Zero setup, instant start, results look professional.

**What makes the UX strong:**
- Reduces the "cold start" problem: default content is pre-populated and looks like a real use case
- The tool feels playful enough to encourage exploration
- Collaboration is the product, not an add-on

**What CarbonRef can reuse:**
→ The demo default values already do this (they calibrate the user's intuition). Go further: make the demo tell a story. Pre-populate a named project ("EMS Les Pins, Vaud") that immediately feels real.
→ Consider a "share this analysis" link — even if CarbonRef is single-user now, the ability to share a snapshot in a meeting changes the value perception.

---

### 3.6 Cliniko / Practice Management — Traffic Light Status with No Ambiguity

**What they do:** Medical practice management. Patient status, appointment scheduling, clinical notes.

**What makes the UX strong:**
- Traffic light indicators that require zero training: red/amber/green always mean the same thing
- Status is the primary element, not the metric that produced it
- Non-expert staff (receptionists) can triage without clinical knowledge

**What CarbonRef can reuse:**
→ The checklist sidebar in Leviers already uses traffic lights — extend this to the Positionnement interpretation panel. The "position label" (au-dessus / dans la zone / sous la cible) should be visually primary, with the number secondary.
→ Non-expert users (MOA, investment committee) will look at color before reading text. Design for that scan order.

---

### 3.7 Autodesk Forma — Environmental Heatmap as Positioning Tool

**What they do:** Overlay environmental analysis (sun, wind, noise) as heatmaps on building massings at schematic stage.

**What makes the UX strong:**
- Spatial positioning: you understand your situation relative to the site, not relative to a spreadsheet
- The heatmap immediately shows "good zones" and "problem zones" without requiring expertise
- The comparison view (before/after intervention) is the core UX move

**What CarbonRef can reuse:**
→ The "zone" logic: CarbonRef's market benchmark ellipse is an implicit heatmap. Make the zone meaning explicit with annotation ("zone marché habituel").
→ Consider a "before/after" view in Scénarios: not just two columns, but a visual shift from current position to scenario position on the cost-carbon chart.

---

### 3.8 GRESB Score — Relative Positioning as Core Value Prop

**What they do:** ESG score benchmarked against peers (same country, same asset type, same fund size).

**What makes the UX strong:**
- The score is meaningless without the peer distribution — and they always show the distribution first
- "Top quartile" is the phrase that gets repeated in LP meetings, not the raw score
- The delta vs prior year is the second most important number

**What CarbonRef can reuse:**
→ The "quartile framing": instead of just "gap vs target," show where this project sits in the distribution ("your project would be in the top 30% of comparable Swiss projects"). This elevates the positioning from compliance to competitive.
→ Year-on-year delta: when CarbonRef is used across multiple projects, the "are we improving?" question becomes available.

---

### 3.9 Notion — Document as Product

**What they do:** Flexible workspace that turned a document editor into a product database.

**What makes the UX strong:**
- Zero distinction between "filling in a form" and "creating a document" — the intake experience is continuous
- Properties are first-class: the metadata is as important as the content
- The blank page isn't intimidating because defaults and templates are offered

**What CarbonRef can reuse:**
→ The Positionnement form should feel less like a form and more like starting a project page. The "Nom de la référence" field in the user baseline is a step in this direction — name the project, make it feel real.
→ Templates: offer two or three preset project profiles ("EMS standard VD," "Logement locatif BE") that pre-populate all fields. Reduces cold-start friction for first-time users.

---

### 3.10 Ramp (Finance) — Decision Embedded in the Workflow

**What they do:** Corporate spend management. Cards, reimbursements, budgets.

**What makes the UX strong:**
- Decisions are embedded in the moment of action — "this expense is 40% over category budget" appears when you submit, not in a monthly report
- The insight is actionable: there's always a "do something" CTA next to the observation
- Non-financial users understand the implications without finance training

**What CarbonRef can reuse:**
→ Every interpretation in CarbonRef should have an embedded CTA. "Votre projet dépasse la cible de 3.5 kgCO₂/m²/an → Voir les leviers disponibles [→]" — the arrow matters.
→ The "gap → lever" connection is CarbonRef's version of Ramp's "over budget → restrict card." Make the causal chain impossible to miss.

---

## 4. SWISS LANDSCAPE

### 4.1 Regulatory context — SIA 390/1 as the anchor

SIA 390/1 (published February 2025 as a full norm, previously a Merkblatt) is now the regulatory reference for greenhouse gas accounting in Swiss construction. It covers the full lifecycle (construction, operation, mobility) and defines the climate pathway for buildings.

Key threshold: **9 kgCO₂e/m²/an** (annualized embodied carbon) is the reference line CarbonRef already uses. This is well-calibrated — it's the number Swiss engineers and MOA are beginning to hear in tender specifications.

Calculation methodology required: SIA 2032 (grey energy LCA method) using KBOB data.

### 4.2 Tools that exist in Switzerland

| Tool | Type | User | Cost axis | Decision-oriented | Swiss-specific |
|------|------|-------|-----------|-------------------|---------------|
| SIA 390/1 Calculation Aid | Calculation aid | Engineers | No | No | Yes |
| Ecotool | Calculation | Engineers | No | No | Partial |
| Lesosai / Enerweb | Detailed LCA | Engineers | No | No | Yes |
| KBOB data (ecobau) | Data reference | Engineers | No | No | Yes |
| ecobau tools (ecoDevis etc.) | Specification | Engineers / planners | Partial | No | Yes |
| REMMS | Sustainability rating | Asset owners | No | Partial | Yes |
| CRREM | Operational pathways | Asset managers | No | Partial | No (Swiss path exists) |
| One Click LCA | Full LCA | Specialists | No | No | No |

**Observation:** Every Swiss tool either (a) requires engineering expertise, or (b) operates at portfolio/operational level. The early-stage, project-level, cost-carbon, decision-oriented layer is **empty**.

### 4.3 Key actors shaping the landscape

**Engineering firms** (Amstein+Walthert, Basler+Hofmann, Rapp Ingénieurs, Pirmin Jung): These firms do embodied carbon consulting as a service. They benefit from the current tool complexity — it keeps carbon assessment a billable deliverable. CarbonRef does not displace them (it operates upstream), but they may perceive it as a threat to their positioning.

**ecobau / KBOB**: The institutional data infrastructure. They publish the LCA data that all Swiss tools use. They do not produce user-facing decision tools. Potential partner / data licensor.

**SIA**: Norm publisher. Not a tool producer. CarbonRef's SIA 390/1 anchoring is a legitimacy play — borrow authority from the norm without competing with SIA directly.

**Minergie**: Certification body. Their label system (Minergie, Minergie-P, Minergie-ECO) is already in CarbonRef's target selector. This is correct — Minergie is the most recognized benchmark for Swiss MOA and is often contractually required.

**Real estate associations** (SVIT, RICS Switzerland, CUREM): These represent the MOA and asset manager constituency. CarbonRef's natural distribution channel.

### 4.4 Where CarbonRef fits

CarbonRef fits in a layer that does not yet exist:

```
[Investment / Faisabilité]   ← CarbonRef lives here
[Esquisse / APS]             ← CarbonRef can extend here
[Avant-Projet]
[Projet]                     ← SIA 390/1 calc aid, Ecotool
[Réalisation]                ← One Click LCA, Tally, detailed LCA
[Exploitation]               ← CRREM, REMMS, energy monitoring
```

The gap exists because:
1. Cost data and carbon data are held by different communities (developers/economists vs. engineers) and no one has bridged them
2. The MOA constituency has not been served — tools have been built for engineers, by engineers
3. The SIA 390/1 norm is new (2025) — the market hasn't caught up yet with decision-oriented tooling

---

## 5. STRATEGIC INSIGHTS

### 5.1 Where is the real gap?

**The gap is not "a carbon tool for Switzerland."** Several of those exist or are entering.

**The gap is:** a tool that lets a non-engineer, in a 20-minute project committee meeting, answer the question: "Is this project on track for our carbon commitments, and what does it cost us to fix it if not?"

This requires:
- Carbon AND cost in the same view
- Relative positioning (not absolute values)
- The user's own baseline as anchor (not just external benchmarks)
- Output that a non-expert can read and act on in real time
- Swiss regulatory anchoring (SIA 390/1)

None of the existing tools provide all five. CarbonRef provides all five by design.

---

### 5.2 Why has no one built CarbonRef yet?

Three structural reasons:

**a) Data fragmentation.** Cost data (CHF/m³ by typology, region, quality level) is commercially sensitive and held by construction economists / entreprises générales. Carbon data (kgCO₂e/m²/an by building type) is held by engineering firms and academic LCA researchers. No one has bridged the two into a single positioning tool — because the two communities don't talk.

**b) Wrong target audience assumption.** Every tool has been built for engineers or sustainability specialists. The MOA and investment committee have been treated as report recipients, not product users. CarbonRef flips this assumption.

**c) Regulatory timing.** SIA 390/1 only became a full norm in February 2025. Before that, there was no enforcement driver. The demand for a pre-LCA decision tool only exists once the norm creates accountability upstream.

---

### 5.3 Biggest risk of confusion

**The "it's an LCA tool" misread.** This is the single most dangerous positioning failure.

If a MOA sees CarbonRef and thinks "I need to call my engineer to use this," the product has failed. If an engineer sees CarbonRef and thinks "this is less precise than my LCA tool," they'll dismiss it.

CarbonRef must make its identity legible in the first 10 seconds:
- It is NOT a calculation tool
- It is NOT a compliance tool
- It IS a decision cockpit for investment-stage conversations

**Tactical implication:** The UI should contain no terminology that engineers use but investors don't. Avoid: "LCA," "EPD," "module A1-A3," "cradle-to-gate." Use: "effort pour atteindre la cible," "impact estimé sur votre budget," "position vs marché."

**Second risk:** Confusion with CRREM. CRREM is now widely used by Swiss institutional investors. CarbonRef must be positioned as "what you use before CRREM becomes relevant" — for new construction decisions, not standing asset monitoring.

---

### 5.4 Positioning statement (candidates)

**Option A (direct):**
> "CarbonRef: l'arbitrage coût-carbone, avant l'architecte."

**Option B (relational):**
> "Sachez où vous en êtes carbone avant de signer le mandat. CarbonRef positionne votre projet en 10 minutes."

**Option C (authority):**
> "Le cockpit de décision carbone pour les maîtres d'ouvrage suisses. Aligné SIA 390/1."

**Recommended:**
> **"Avant l'étude LCA, avant le mandat — savoir si votre projet est carbone-compatible."**

Rationale: names the moment (pre-LCA, pre-mandate), names the user need (knowing), names the relevant constraint (carbon-compatible), avoids jargon. Positions CarbonRef upstream of every existing tool.

---

### 5.5 Competitive moat hypotheses

- **Swiss data specificity**: KBOB-calibrated benchmarks, CHF/m³ Swiss market ranges, SIA 390/1 threshold — not replicable by US tools without significant localization effort
- **The "user baseline" concept**: No competitor anchors positioning in the user's own historical performance. This is defensible as a UX patent and a network effect (the more projects a user runs, the richer their baseline)
- **Non-expert target**: Going upstream of LCA tools means CarbonRef competes for a budget line (investment decision support, ESG strategy) rather than a tool replacement budget (LCA software)
- **Decision meeting context**: If CarbonRef becomes the thing people open in investment committee meetings, it becomes sticky by habit and social proof, not by lock-in

---

## 6. BONUS — Reverse Engineering REMS-like Tools

*Strategy to extract insight from a gated tool without copying.*

### 6.1 The goal

You're not trying to copy the UI. You're trying to understand:
1. What mental model does it embed? (What does it assume users care about?)
2. How does it handle uncertainty and missing data?
3. How does it translate complex inputs into a decision-ready output?
4. What does it NOT show, and why?

### 6.2 Structured session protocol

**Session 1: Inputs audit (15 min)**
- List every input field. Note: which are required vs optional? Which have defaults? Which use qualitative scales vs numbers?
- Screenshot the intake form in full. Annotate each field with: "Who would know this?" (engineer / developer / MOA / nobody)
- Hypothesis: the inputs that non-experts can answer reveal the tool's true audience

**Session 2: Outputs audit (15 min)**
- Capture every output screen. Note: what is shown first? (primary output) What requires drilling? (secondary)
- For each number shown: is it absolute or relative? Does it have a target or benchmark attached?
- Note the vocabulary used — expert or non-expert?

**Session 3: Uncertainty handling (10 min)**
- Enter intentionally incomplete / inconsistent data. What happens?
- Does the tool show confidence intervals, ranges, or flags?
- Does it prevent submission or allow partial analysis?

**Session 4: The "so what" test (10 min)**
- After running a full scenario: what is the tool's answer to "what should I do now?"
- Is there a CTA, a recommendation, a next step embedded in the output?
- If not: that's your gap. CarbonRef fills it.

### 6.3 Translation framework

For each observation, ask: "What does this imply about the user's mental model?"

| Observation | Mental model implication | CarbonRef implication |
|-------------|--------------------------|----------------------|
| Tool requires kWh/m² input | User is an energy engineer | CarbonRef should NOT require this — use qualitative proxy |
| Tool shows absolute values without benchmark | User already knows what "good" looks like | CarbonRef's benchmark ellipse is more powerful than any absolute value |
| Tool has no cost output | Carbon and cost are separate concerns for this tool's user | This is CarbonRef's core differentiator — bundle them |
| Tool requires login to see results | Business model is lead generation / gated | Consider CarbonRef's own friction strategy |
| Tool produces PDF report | Decision is made elsewhere (in a meeting, not in the tool) | CarbonRef's export CTA is critical — Synthèse should be the shareable artifact |

### 6.4 What to bring back

Not: specific UI patterns (risk of infringement, risk of copying the wrong thing)

Yes:
- The list of inputs non-experts can actually answer vs. those they can't
- The vocabulary the tool uses — and what it avoids
- The primary output format (score / position / recommendation)
- The "biggest confusion moment" (where you had to think twice — that's where CarbonRef can do better)

---

*Document end — Version 1.0, April 2026*
*Next update: after user testing sessions and REMS session review*

---

## ADDENDUM — Keevalue × Popety Stack (April 2026)

*Added before Bus Dev call — critical intelligence*

---

### Keevalue.ch — ⚠️ The Most Strategically Significant Swiss Actor

**What they are:** Swiss construction cost estimation platform, founded 2014 by architects. CEO: **Stefan Cadosch — former president of SIA**. Based in Brugg (Aargau).

**Core product:** Construction cost estimation from first sketch to demolition, per building element, per year. Regional differentiation (Zurich ≠ Bern ≠ Ticino). Claims < 10% deviation from actual costs on a dataset of completed Swiss projects.

**What they cover:**
- CHF/m² and CHF/m³ SIA by building type and region — the exact cost data CarbonRef uses as an axis
- Operating costs (Betriebskosten)
- Energy, water, and **CO₂ benchmarks** — they already track carbon, even if secondary
- BIM integration: real-time cost + CO₂ delta per design change

**Target users:** Architects, planners, and Bauherren (MOA) — same as CarbonRef.

**The CEO factor is critical.** Cadosch as former SIA president means:
- Maximum regulatory legitimacy in Switzerland
- Deep relationships with SIA norm-setting bodies (SIA 390/1 is directly in his orbit)
- Distribution access to architects and engineering firms that CarbonRef currently lacks
- He could add a carbon positioning layer to Keevalue's cost tool and be the most credible actor in the Swiss market to do so

---

### Popety.io — Land Prospecting Layer

**What they are:** Swiss proptech, focused on identifying underexploited plots for development. Core product: "LandDev" — aggregates official Swiss data (federal, cantonal, municipal) to rate plots for development potential.

**Coverage:** French-speaking Switzerland (GE, VD, FR, VS, NE, JU) + ZH, BS, BE.

**Investor:** Romande Energie (utility, 6.45% stake, Jan 2024) — signals an energy/sustainability angle.

**Four pillars:** Explore (plot rating) → Analyse (key plot data) → Share (export) → Alerts (monitoring).

**What they don't have:** construction cost estimates, carbon analysis — hence the Keevalue partnership.

---

### The Keevalue × Popety Stack

What this partnership creates:

```
[Land opportunity]     ← Popety (plot rating, zoning, potential)
[Construction cost]    ← Keevalue (CHF/m³, by type and region)
[Carbon positioning]   ← ??? — the missing layer
```

Together, they are building a **feasibility cockpit for Swiss developers** at the earliest project stage. This is the same user, the same moment, and the same workflow as CarbonRef.

**The gap they leave:** neither Popety nor Keevalue positions the project relative to carbon targets (SIA 390/1, Minergie). Their joint stack answers "can I build this, and how much will it cost?" but not "will this project be carbon-compatible, and what's the cost of making it so?"

**That is CarbonRef's exact opening.**

---

### Strategic Options Going Into the Call

**Option A — Partner / API integration**
CarbonRef plugs into the Keevalue cost data as its cost axis benchmark, and provides the carbon positioning layer to the Keevalue-Popety stack. Division of labor: Keevalue owns cost, CarbonRef owns carbon + decision UX.

*Upside:* Keevalue's dataset solves CarbonRef's hardest data problem (real CHF/m³ benchmarks). Distribution via Popety's developer user base.
*Downside:* Dependency risk. If Keevalue decides to build the carbon layer themselves, CarbonRef loses its differentiation.

**Option B — White-label / embedded module**
CarbonRef's cost-carbon positioning view becomes an embedded tab inside the Popety webapp, powered by Keevalue cost data.

*Upside:* CarbonRef doesn't need to build distribution; Popety has the developer audience.
*Downside:* Loss of brand; pricing and margin controlled by Popety.

**Option C — Co-exist, differentiate clearly**
CarbonRef targets a different buyer (MOA investment committee, asset owner) rather than the developer/broker that Popety serves. Different moment in the project lifecycle, different decision.

*Upside:* No dependency, full control of positioning.
*Downside:* Harder distribution path; parallel market development.

**Option D — Keevalue as the acquirer / data licensor**
Keevalue licenses their CHF/m³ dataset to CarbonRef in exchange for the carbon positioning layer, co-branded or co-developed.

*This may be the most durable structure* — Keevalue gets a carbon product without building it, CarbonRef gets Swiss cost data without collecting it.

---

### Call Prep: Questions to Probe

**On Keevalue's carbon ambition:**
- "Vous avez déjà des données CO₂ dans votre plateforme — est-ce que vous avez un projet de les rendre plus décisionnelles ?"
- "Est-ce que vous travaillez avec SIA 390/1 comme référence pour votre couche carbone ?"

**On the Popety partnership scope:**
- "Le partenariat avec Popety — c'est une API, un white-label, ou une co-vente ?"
- "Qui est le client final : le promoteur, le broker, ou le MOA ?"

**On the gap they know they have:**
- "Dans votre outil actuel, est-ce qu'un utilisateur peut voir si son projet est compatible avec des objectifs carbone ?"
- (If no:) "Est-ce que c'est un besoin que vous entendez de vos clients ?"

**On partnership appetite:**
- "Est-ce que vous avez réfléchi à intégrer une couche de positionnement carbone dans votre workflow ?"

**What NOT to reveal at this stage:**
- The details of CarbonRef's benchmark data sources (keep data layer ambiguous)
- Any pricing structure
- The fact that CarbonRef's benchmarks are currently manually calibrated rather than live API-fed
