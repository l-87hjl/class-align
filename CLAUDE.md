# CLAUDE.md — class-align

Teacher-facing system for standards-aligned rubric grading, teacher-clarity
support, batch assignment processing, and longitudinal standards-coverage
memory. Classes: 10th CP (priority 1), 11th CP (priority 2), 9th CP
(deferred). The teacher's established methods are authoritative — never
substitute generic definitions for Teacher Clarity, Visual Learning, or the
rubric system.

## Mandatory reads, in order

1. This file
2. PROJECT_STATE.md (current state — rehydrate before acting)
3. docs/solutions/GC_RUBRIC_SOLUTION.md (before ANY rubric work — never
   re-derive the import format or toolchain)
4. For design work: docs/plans/implementation-plan.md
5. For deep intent: develop/planning/initial/012 (summary), then others as
   needed (they are context, not implementation dictates)

## HARD PRIVACY RULES (student data — non-negotiable)

1. **`protected/` is the ONLY location for any student work or student-
   derived material. It is gitignored; nothing under it is ever committed,
   pushed, or exposed via any interface.** Verify with `git status` after
   any work session that touched it.
2. Student exemplars enter ONLY after anonymization AND an identifier
   preflight check (names, usernames/emails, ID numbers, identifying
   teacher comments, file metadata/document properties, classmates' names,
   contextual identifiers). Check outcome is three-state: clean / possible
   identifiers — teacher review / definite identifiers — blocked. The
   teacher is always the final reviewer; automated checks are safeguards,
   not guarantees.
3. Full source texts (novels, readings) are protected material: never
   public-web-exposed, never committed if licensing is unclear —
   `protected/` or reference-by-path.
4. Generated artifacts (rubrics, clarity docs, standards analyses) built
   from teacher-authored content are normally safe to commit; anything
   quoting student work is not.
5. Anonymization is never assumed complete because a name was removed.
   When in doubt → `protected/` + flag for teacher review.

## Layout

- `docs/solutions/` solved operational knowledge (GC rubric format, etc.)
- `docs/plans/` implementation plan + progress log
- `docs/intake/` transfer-folder intake procedure
- `sources/authoritative/` canonical method docs + working template (the
  teacher's system; treat as spec, version don't overwrite)
- `sources/classes/{10cp,11cp,9cp}/` per-class materials (from intake zips)
- `user-uploads/` original uploads as received (provenance; read-only)
- `registry/` standards-coverage registry (longitudinal memory)
- `outputs/` generated per-assignment packages
- `protected/` student data + protected texts (GITIGNORED)
- `develop/planning/initial/` intent notes 001–012 (context, not spec)

## Operating rules

- Git identity `102322814+l-87hjl@users.noreply.github.com`; non-interactive
  commands; seed-commit early; push incrementally; update PROJECT_STATE.md
  at session end.
- Findings routing per metaOps FINDINGS_TRACKER practice; packets to/from
  other repos per metaOps intake-packet conventions.
- Rubric scale semantics everywhere: 3 = meets = success; ordinal, never
  percentage. Holistic carries the grade weight and stays teacher-owned.
