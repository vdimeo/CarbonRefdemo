# CarbonRef — Prompt Library

## 🔗 Context global (à réutiliser partout)

Context:
- Product spec: https://raw.githubusercontent.com/vdimeo/CarbonRefdemo/main/carbonref_spec.md
- Current HTML: https://raw.githubusercontent.com/vdimeo/CarbonRefdemo/main/index.html
- UX Journal: https://raw.githubusercontent.com/vdimeo/CarbonRefdemo/main/carbonref_ux_journal.md

Instructions:
- Always read ALL documents before answering
- Do NOT hallucinate missing parts
- Work only with existing structure unless explicitly asked otherwise

---

# 🧠 1. Prompt — Update UX Journal (incremental only)

Context:
my product spec is at https://raw.githubusercontent.com/vdimeo/CarbonRefdemo/main/carbonref_spec.md  
the current HTML is at https://raw.githubusercontent.com/vdimeo/CarbonRefdemo/main/index.html  
the UX journal is at https://raw.githubusercontent.com/vdimeo/CarbonRefdemo/main/carbonref_ux_journal.md  

Please read all three before answering.

My request:
Update the UX journal based on the following inputs:

[PASTE NEW UX INSIGHTS HERE]

Constraints:
- DO NOT rewrite the whole document
- ONLY add or modify the relevant sections
- Preserve the existing structure and wording as much as possible
- Add new elements in the appropriate sections:
  - Hypothèses clés
  - Décisions prises
  - Questions ouvertes
  - Tests utilisateurs
- Be concise and structured

Output format:
- Return only the modified parts
- Use markdown
- Clearly indicate where additions should be inserted

---

# 🛠️ 2. Prompt — Apply changes to full UX Journal

Context:
my UX journal is at https://raw.githubusercontent.com/vdimeo/CarbonRefdemo/main/carbonref_ux_journal.md  

Please read it before answering.

My request:
Here is a set of updates to apply:

[PASTE PATCH / MODIFICATIONS HERE]

Constraints:
- Apply the changes directly into the full document
- Preserve formatting and structure
- Ensure consistency across sections
- Do not remove existing content unless explicitly specified

Output format:
- Return the FULL updated markdown file
- Clean, ready to commit (no explanations)

---

# 📐 3. Prompt — Update Spec (incremental)

Context:
my product spec is at https://raw.githubusercontent.com/vdimeo/CarbonRefdemo/main/carbonref_spec.md  

Please read it before answering.

My request:
Update the spec based on the following changes:

[PASTE SPEC CHANGES HERE]

Constraints:
- DO NOT rewrite the full spec
- ONLY modify relevant sections
- Keep naming and structure consistent
- Avoid duplications

Output format:
- Return only the modified parts
- Use markdown diff style if relevant

---

# 🧩 4. Prompt — Apply changes to full Spec

Context:
my product spec is at https://raw.githubusercontent.com/vdimeo/CarbonRefdemo/main/carbonref_spec.md  

Please read it before answering.

My request:
Apply the following updates to the full spec:

[PASTE PATCH HERE]

Constraints:
- Integrate changes cleanly
- Maintain internal consistency
- Do not break section numbering

Output format:
- Return FULL updated spec
- Clean markdown, ready to commit

---

# 🔀 5. Prompt — Generate clean diff

You are updating an existing markdown product spec.

## Context

Original spec:
https://raw.githubusercontent.com/vdimeo/CarbonRefdemo/refs/heads/main/carbonref_spec.md

Requested changes:
{{PASTE CHANGES OR PATCH}}

## Your task

Apply the requested changes **directly into the original spec**.

## CRITICAL RULES

- DO NOT rewrite the document
- DO NOT change structure, section names, or ordering unless explicitly required
- DO NOT rename sections (e.g. "Data model" ≠ "Data & Metrics")
- DO NOT rephrase existing content unnecessarily
- DO NOT duplicate content
- ONLY:
  - insert new sections where relevant
  - modify existing lines where explicitly required

- If a section already exists:
  → update it, do not recreate it

- If structure differs from the patch:
  → ADAPT the patch to the existing structure (do not force it)

## Output requirements

- Return the FULL updated markdown file
- Keep formatting clean and consistent
- No explanations
- No comments
- No placeholders

## Quality check before output

Ensure:
- The original structure is preserved
- No section was accidentally renamed or duplicated
- All requested changes are applied
- The document remains coherent

# 🔧 6.PROMPT — Apply Diff (Strict & Safe)

You are applying a unified diff to an existing file.

## Context

Original file:
https://raw.githubusercontent.com/vdimeo/CarbonRefdemo/refs/heads/main/carbonref_spec.md

Diff to apply:
{{PASTE DIFF}}

## Your task

Apply the diff EXACTLY to the original file.

## CRITICAL RULES

- DO NOT rewrite the file
- DO NOT reformat anything
- DO NOT change indentation, spacing, or line breaks
- DO NOT fix or improve the content
- DO NOT interpret intent

- ONLY:
  - remove lines marked with `-`
  - add lines marked with `+`
  - keep all other lines STRICTLY identical

## MATCHING RULES (VERY IMPORTANT)

- A `-` line MUST match EXACTLY a line in the original file
- If it does not match exactly:
  → DO NOT GUESS
  → DO NOT APPLY that change

- Apply changes ONLY where the match is exact
- Preserve original ordering and structure

## AMBIGUITY HANDLING

If:
- multiple possible match locations exist
- or a line cannot be matched exactly

→ SKIP that specific change (do not hallucinate placement)

## OUTPUT FORMAT

Return ONLY the modified parts using unified diff format:

```diff
--- original
+++ updated
@@
- old line
+ new line```

# 🔧 7.PROMPT — Generate HTML Patch from Spec (No Rewrite)

You are modifying an existing HTML prototype.

## Context

Current HTML file:
{{PASTE CURRENT HTML FILE}}

Updated product spec:
{{PASTE UPDATED SPEC}}

UX journal, if needed:
{{PASTE UX JOURNAL OR LINK}}

## Your task

Identify the minimal HTML/CSS/JS changes required to make the current HTML comply with the updated spec.

## CRITICAL RULES

- DO NOT rewrite the full HTML file
- DO NOT redesign the UI
- DO NOT rename existing functions, variables, IDs, classes, tabs, or sections unless explicitly required by the spec
- DO NOT remove existing functionality unless explicitly required
- Reuse the existing design system, components, chart logic, and data structures as much as possible
- Add only what is missing
- Modify only what conflicts with the updated spec
- Preserve formatting style and coding conventions from the existing file

## PATCH STRATEGY

Before writing code:
- Compare the updated spec against the current HTML
- Identify:
  - new UI elements to add
  - existing UI elements to modify
  - data model changes
  - chart changes
  - labels/units to update
  - interaction changes
- Ignore anything already implemented correctly

## OUTPUT FORMAT

Return ONLY a unified diff patch:

```diff
--- index.html
+++ index.html
@@
- old line
+ new line


---

# 🔧 PROMPT — Apply HTML Patch Safely

You are applying a patch to an existing HTML file.

## Context

Original HTML file:
{{PASTE CURRENT HTML FILE}}

Patch to apply:
{{PASTE PATCH}}

## Your task

Apply the patch to the original HTML file.

## CRITICAL RULES

- DO NOT rewrite the HTML file from scratch
- DO NOT reformat unrelated code
- DO NOT rename variables, functions, classes, IDs, or tabs
- DO NOT improve or simplify code beyond the patch
- DO NOT infer missing changes
- ONLY apply the patch

## MATCHING RULES

- Removed lines marked with `-` must match the original HTML exactly
- Added lines marked with `+` must be inserted exactly where the patch indicates
- If a patch block cannot be matched with high confidence:
  - DO NOT guess
  - leave that block unapplied
  - report it under `UNAPPLIED BLOCKS`

## OUTPUT FORMAT

Return the FULL updated HTML file.

## STRICT OUTPUT RULES

- No explanations before or after
- No markdown wrapper
- No commentary
- Preserve the existing file structure
- Preserve unrelated whitespace and indentation

## FINAL CHECK

Before output, ensure:
- All safely applicable patch blocks were applied
- No unrelated code changed
- The resulting file is valid HTML
- Existing JS functions remain intact
