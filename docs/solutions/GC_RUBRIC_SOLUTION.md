# GC Rubric Solution — Google Classroom Import Format (SOLVED — do not re-derive)

**Produced by: Claude Fable 5**, reconstructed from the working artifacts.
Status: OPERATIONAL v1.0, 2026-07-22. This is the permanent record of the
solved problem "produce a rubric file Google Classroom will import."
Authoritative sources (preserve, never casually rewrite):
`user-uploads/GC_Rubric_Directions_CURRENT_v01.08 (1).md` (method + workflow),
`GC_Rubric_Template_STRUCTURE (1).md` (layout guide),
`GC_Rubric_Template_WORKING (1).xlsx` (the known-good import file — START
FROM THIS, always).

## The solved format, exactly

An importable Google Classroom rubric spreadsheet (.xlsx) is:

```
Row 1, col A: It is recommended that you do not edit rubrics in spreadsheet format.
Row 2, col A: v1.0-s
Then one 5-row block PER CRITERION, no blank rows between, no header row:
  Block row 1 (col A): Criterion title
  Block row 2 (col A): Criterion description
  Block row 3 (cols B–F): Level POINT VALUES, descending (e.g. 4 3 2 1 0)
  Block row 4 (cols B–F): Level NAMES (Advanced | Proficient | Progressing |
                          Developing | Missing / Not Assessable)
  Block row 5 (cols B–F): Level DESCRIPTIONS
```

Column A of rows 3–5 stays EMPTY. No merged cells, no formatting tricks,
no extra notes, no "Criteria/Level" header table — any of those break import.
Max 10 criteria per rubric (Google Classroom hard limit).

## The rubric method (teacher's system, from directions v01.08)

1. One 0–4 criterion per clearly-warranted CA CCSS standard; title begins
   with the standard code (`RL.9-10.2 - Theme / Central Idea Development`)
   so it can be linked to the tagged learning goal. Standards count is
   assignment-driven — NEVER default to 4; max 9 (+1 holistic = 10).
2. One holistic criterion takes ALL remaining points:
   `Holistic = Total − (standards × 4)`, levels at **100% / 85% / 75% /
   63% / 0%** of the HOLISTIC value (not the assignment total). Round only
   if import requires; preserve the pattern. Holistic stays UNLINKED to any
   standard.
3. Scale semantics: **3 = Proficient = met the standard = full ordinary
   credit expectation. 4 = Advanced, never a hidden requirement.** Levels
   are ordinal descriptors, NOT percentages — any tool (esp. AI graders
   like Wayground) treating 3/4 as 75% is wrong and must be corrected via
   explicit level descriptions.
4. Gradebook offset when standards-linking compresses grades:
   `offset = 2 × tagged standards` as extra credit (Aeries comment
   documented in directions §9). Not part of the rubric file.
5. Teacher tags standards in Google Classroom FIRST; then manually links
   each standards criterion to its goal during rubric attach; holistic
   unlinked.

## Exact production steps (no re-derivation)

1. Copy `GC_Rubric_Template_WORKING (1).xlsx` (or its canonical copy in
   `sources/authoritative/`). Never build a spreadsheet from scratch.
2. Compute content first: standards list, criterion titles/descriptions,
   holistic points + 100/85/75/63/0 spread, verify total = assignment value.
3. Edit with **openpyxl** (or current environment's xlsx tool), replacing
   CONTENT ONLY — template structure, blocks, and empty cells untouched.
   Add/remove whole 5-row blocks to change criterion count.
4. Verify (§Checklist below) before delivery.
5. Teacher-side: upload to Drive → open with Google Sheets → Classroom
   rubric import ("Create rubric → Import from Sheets"). The file must be
   a native Google Sheet at import time; the xlsx→Sheets conversion is
   part of the teacher's flow.

## Verification checklist (run every time)

- [ ] Rows 1–2 exactly as specified (verbatim strings)
- [ ] Every criterion is a clean 5-row block; col A empty in rows 3–5
- [ ] Point values descending; standards rows 4/3/2/1/0
- [ ] Holistic = total − 4×standards; spread 100/85/75/63/0 of holistic
- [ ] Grand total = requested assignment value
- [ ] ≤ 10 criteria including holistic
- [ ] No merged cells / headers / notes / formulas / extra sheets touched
- [ ] Standards criterion titles start with the CA CCSS code
- [ ] Level descriptions state that 3 = meets the standard (guards AI
      graders against percentage misreading)

## Gotchas (each cost real time once — never again)

1. **Generic tables don't import.** A normal Criteria/Levels header table
   fails; only the 2-header-rows + 5-row-block format works.
2. **The TSV is a shadow, not the source.** The tsv export flattens the
   xlsx; regenerate FROM xlsx, never treat tsv as authoritative (planning
   doc 006). The working 20pt tsv in user-uploads shows holistic levels
   4/3.4/3/2.5/0 — note 2.5 vs the formula's 2.52: import rounding of the
   63% level. Preserve the pattern, round only as needed.
3. **AI graders misread ordinals as percentages** and under-score the
   holistic row (~C-work → 70% reasoning). Fix is in the DESCRIPTIONS:
   state completion-based meaning explicitly (planning doc 010).
4. **Tool drift is the meta-gotcha.** Agents kept re-figuring the toolchain
   because instructions lived in chat context. THIS doc + the template
   copy in-repo are the fix: the workflow is repo-resident, tool-agnostic
   (any xlsx-capable tool), and template-first. Directions v01.08 §"check
   current tool instructions" still applies for the executing environment.
5. **Examples read as requirements.** All example lists in generated
   rubric text must use "including but not limited to" phrasing (v01.07
   rule) or students/graders treat them as exhaustive.
