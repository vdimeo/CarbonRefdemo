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

Context:
original file and updated file will be provided

My request:
Generate a clean diff between the two versions

Constraints:
- Use standard diff format
- Keep it readable
- Focus only on meaningful changes (ignore whitespace if possible)

Output format:
```diff
--- original
+++ updated
@@
- old line
+ new line
