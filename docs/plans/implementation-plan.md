# Implementation Plan — class-align

**Produced by: Claude Fable 5** (design authority per Geoff's delegation).
Status: v1.0. Date: 2026-07-22. Tiers: S = Sonnet-class (strict spec),
O = Opus/GPT-high (implementation from spec), F = Fable-class (judgment).
Token estimates = rough end-to-end session cost.

## Design shape (decisions, not options)

**Repo-first, batch-first, interface-later.** The system of record is THIS
repo: normalized assignment records, the standards registry, and generated
output packages — all reviewable as files, versioned by git, operable by
any agent (chat/CLI). The batch pipeline runs on the Mac mini now; a web
interface (Render or Mac-mini-backed, planning doc 004's boundary models)
is Phase C4, decided only after the pipeline proves itself. This resolves
the planning docs' deployment question in favor of value-now: everything
the teacher gets in v1 is a file package he can use in Google Classroom
immediately, produced in batches without per-assignment prompting.

**Pipeline per assignment group:**
`intake → group → analyze (standards per selection priorities) → generate
(rubric xlsx per GC_RUBRIC_SOLUTION + clarity summary + visual-learning
package + copy-paste blocks) → validate (format checker + coverage check)
→ registry update → output package for teacher review`.

**Data model:** one folder per assignment under `outputs/<class>/<slug>/`
containing `assignment.yaml` (id, class, year, source files, status),
`standards.yaml` (selections with role: primary/specific/supporting +
rationale + teacher-confirmed flag), rubric.xlsx, clarity.md, visual.md,
gc-blocks.md (title/directions/CA-CCSS paste block), review-notes.md.
`registry/standards_registry.yaml` aggregates: per-standard appearances,
roles, assignments, parent rollup — answers the coverage questions in
planning doc 008 directly from the repo.

**Grading semantics enforced in code (v2 per ADR-0001):** standards rows
0–3 with **Meets = 3 = row max = full credit** (percentage misreading
structurally impossible); holistic = total − 3×n at 100/85/75/63/0; the
former +2/standard offset is RETIRED. Advanced survives only as the
aspirational WAGOLL tier in visual-learning outputs and unscored
recognition. WP specs must consume docs/plans/changes-from-planning-notes.md
rows before delegation (that table is the delegation checklist).

## Work packages

### Phase C0 — Foundations (partly done this session)

| WP | What | Tier | Est |
|----|------|------|-----|
| C0.1 | GC solution doc + onboarding (DONE 2026-07-22) | F | done |
| C0.2 | Rubric format validator: script checking GC_RUBRIC_SOLUTION v2 checklist against any .xlsx (openpyxl; fixtures incl. v1 template AND v2 fixtures; MUST include the ADR-0001 misreading regression case — percentage-logic grader awards full credit to meets on v2, under-awards on v1) | O | ~1–2M |
| C0.4 | Produce GC_Rubric_Template_WORKING_v2.xlsx: copy v1 template, standards blocks → 4 levels `3 2 1 0` with "Meets the Standard — Full Credit" top level, ADR-0001 descriptors; validate with C0.2; one manual GC import test by Geoff before it becomes canonical | O build, Geoff verify | ~1M |
| C0.3 | Anonymization preflight checker: three-state identifier scan (names/emails/IDs/metadata) for files headed to protected/ | O | ~2–3M |

### Phase C1 — Intake & corpus

| WP | What | Tier | Est |
|----|------|------|-----|
| C1.1 | Class-zip intake per docs/intake/INTAKE.md + corpus inventory (per-class file listing, type histogram, md conversion queue) | S | ~0.5–1M |
| C1.2 | Assignment grouping pass: cluster loose files into assignment groups w/ confidence; teacher-review list for ambiguous (planning doc 009) | O | ~2–4M |
| C1.3 | Doc→markdown normalization (docx/pdf/slides→md; reuse g2brain/marker chunking playbook approach) | O | ~2–3M |

### Phase C2 — The batch pipeline (core value)

| WP | What | Tier | Est |
|----|------|------|-----|
| C2.1 | Standards analyzer: CA CCSS selection per directions §1 + planning-doc-008 priorities (anchor → specific substandard → supporting → SL/L attention checks), rationale per pick, registry context | O | ~3–5M |
| C2.2 | Rubric generator: template-copy + openpyxl content fill per GC_RUBRIC_SOLUTION; C0.2 validator gate; unit fixtures at 20/50/100/200 pts, 2–9 standards | O | ~2–4M |
| C2.3 | Clarity + visual-learning generator per the v3 prompt template in sources/authoritative (admin summary + whiteboard WHAT/WHY/HOW/MODEL + model progression Advanced→No Evidence) | O | ~2–4M |
| C2.4 | Output-package assembler + gc-blocks.md (title, directions, CA CCSS paste list per directions §2) + review-notes | S | ~1M |
| C2.5 | Registry updater + coverage report (per-standard counts, roles, parent rollup, underrepresented strands incl. SL/L) | O | ~2–3M |
| C2.6 | Batch runner: resumable over N assignment groups, per-group manifest, failure isolation (one bad group never kills the batch) | O | ~2–3M |
| C2.7 | First real batch on 10th-grade corpus + teacher review round; capture corrections as fixture/spec updates | F review, O run | ~2–4M |

### Phase C3 — Grading support (after C2 proves out)

| WP | What | Tier | Est |
|----|------|------|-----|
| C3.1 | Wayground-facing level-descriptor emphasis (explicit anti-percentage language in descriptions) + teacher override recording in assignment.yaml | O | ~1–2M |
| C3.2 | Student-exemplar workflow: protected/ intake → C0.3 preflight → teacher approval → anonymized model linkage to assignments | O | ~2–3M |
| C3.3 | ~~Meets-capped vs offset decision~~ RESOLVED by ADR-0001 (2026-07-22): scored Advanced removed, offset retired. Residual: optional grade-impact backcheck on first real batch comparing v1-with-offset vs v2 outcomes | O (optional) | ~0.5M |

### Phase C4 — Interface (deferred by design)

| WP | What | Tier | Est |
|----|------|------|-----|
| C4.1 | Access-boundary decision (Render vs Mac-mini-backed vs hybrid) revisited with real usage data | F | ~0.5M |
| C4.2 | Thin interface over the pipeline (upload → batch → download packages), auth, protected-storage boundary per planning doc 004 | O | ~5–10M |

## Sequencing

C0.2 → C1.1 (blocked on zip arrival) → C1.2/C1.3 → C2.1–C2.6 → C2.7
(teacher round) → C3.x. C0.3 anytime before any student material arrives.
Totals: F ≈ 1–2M remaining; O ≈ 25–40M; S ≈ 1.5–2M.

## Findings routing

Sua-sponte findings → metaOps FINDINGS_TRACKER practice; anything touching
other repos via intake packets. Rubric-format discoveries append to
GC_RUBRIC_SOLUTION.md gotchas (F-tier edit), never live only in chat.
