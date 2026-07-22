# ADR-0001 — Remove the Scored "Advanced" Level from Standards Criteria

Status: ACCEPTED (Geoff, 2026-07-22). **Recorded by: Claude Fable 5.**
Supersedes: the 0–4 standards scale in GC_Rubric_Directions v01.08 and the
+2/standard extra-credit offset (directions §9).

## Decision

Standards-based rubric criteria use a **4-level, 0–3 scale where Meets the
Standard = 3 = the row maximum = 100% of the criterion's points.**

| Points | Level name (import text) | Meaning |
|---|---|---|
| 3 | Meets the Standard — Full Credit | Expected successful competency; highest scored level |
| 2 | Progressing | Partially meets; general/uneven/incomplete |
| 1 | Developing | Limited evidence |
| 0 | Missing / Not Assessable | No assessable evidence |

Holistic criterion: unchanged 5-level structure at 100/85/75/63/0% of the
holistic value; `Holistic = Total − (3 × standards)`. The extra-credit
offset is ELIMINATED — nothing is owed and nothing is silently lost.

The proficient-vs-advanced distinction SURVIVES as an unscored,
aspirational artifact: the visual-learning WAGOLL progression keeps all
five tiers (Advanced → No Evidence of Skill) with adjacent-level
comparisons, and reviewers may add unscored "advanced work" recognition in
feedback/review-notes. It just never appears as a scored rubric level.

## Rationale (Geoff's, from planning notes 007/010 + direct instruction)

1. College-prep, not AP: meeting the standard IS full credit; an advanced
   scored tier makes mastery a hidden requirement or an accounting burden.
2. AI-grader failure mode: any scale where meets < max invites
   "N-of-max = percentage" misreading (3/4 → ~75% → award 2). The fix must
   be STRUCTURAL: with meets = max, percentage logic yields 100% for
   competent work — the misreading is impossible by construction, not by
   descriptor pleading. (Descriptors still state it; defense in depth.)
3. Offset awkwardness: with Advanced scored, an 8-standard rubric forces
   either 16 owed extra-credit points or silent loss. Removing the tier
   removes the bookkeeping.
4. Aspiration belongs in models, not scoring: WAGOLL progression shows
   students what stronger work looks like without grading them against it.

## Consequences

- GC import mechanics unchanged (5-row blocks); standards points row is
  now `3 2 1 0` across columns B–E (four levels — Google Classroom
  supports variable level counts per criterion).
- Working template needs a v2 (WP C0.4): 3-level-capped standards blocks;
  v01.08 template preserved as the v1 historical record.
- Registry/coverage semantics unaffected (meets-rate still visible; an
  unscored "advanced observed" flag MAY be recorded in assignment.yaml
  for information only).
- Wayground/AI grading instructions simplify: "highest level = full
  credit = meets" is now self-evident from the scale.
- Directions doc supersedence: v01.08 remains the baseline record; the v2
  method lives in docs/solutions/GC_RUBRIC_SOLUTION.md §v2. Any future
  regenerated teacher-facing directions doc must be built from v2.

## Tested-against requirement

Fixture suite (WP C2.2) MUST include the misreading case: a simulated
grader applying percentage logic to a v2 rubric must produce 3 (full
credit) for meets-level work; a v1-format rubric fixture is retained as
the regression contrast demonstrating why the change was made.
