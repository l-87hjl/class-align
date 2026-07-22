# PROJECT_STATE — class-align

Updated: 2026-07-22 (Fable onboarding session). Update at every session end.

## Where the project stands

- Planning phase complete: intent notes 001–012 in develop/planning/initial/
  (written as context by another AI; implementation deliberately deferred
  to this repo's design docs).
- **GC rubric import problem: SOLVED and recorded** —
  docs/solutions/GC_RUBRIC_SOLUTION.md. Never re-derive.
- Onboarding structure in place (this session): layout per CLAUDE.md,
  privacy rules baked in, authoritative sources promoted to
  sources/authoritative/.
- Implementation plan: docs/plans/implementation-plan.md (tiered WPs).
- Intake: awaiting Geoff's two class-template zips → see docs/intake/INTAKE.md
  for the watched transfer folder and landing procedure. NOT YET ARRIVED
  as of 2026-07-22. UPDATE: arrived + processed 2026-07-22, three zips.

## Immediate next actions (in order)

1. When zips arrive: run intake per docs/intake/INTAKE.md (unpack to
   sources/classes/{10cp,11cp}/, inventory, commit).
2. Execute WP C1.1 (corpus inventory + assignment grouping) on the
   unpacked materials.
3. Then WP C2.x rubric-generation pipeline per the plan.

Intake COMPLETE 2026-07-22: 175 template files across 10cp/11cp/9cp (see
per-class INTAKE_RECORD.md); 4 full-text novels in protected/; C1.1
corpus inventory partially satisfied, C1.2 grouping is next.

## Precedence + decisions

- **Precedence (Geoff, 2026-07-22): planning/initial notes = CURRENT
  intent, supersede user-uploads baseline wherever divergent.** Divergence
  catalog: docs/plans/changes-from-planning-notes.md (20 items, statused).
- **ADR-0001 ACCEPTED**: scored Advanced removed; standards rows 0–3 with
  Meets = max = full credit; offset retired; Advanced is WAGOLL-only.
  Solution doc is now v2.

## Open questions (route to Geoff / F-tier)

- Exact rubric descriptor WORDING per class (verify against incoming class
  templates; scale itself is settled by ADR-0001).
- C0.4 template v2 needs Geoff's one manual GC import test before it
  becomes canonical.
- Deployment surface (Render web vs Mac-mini-local vs hybrid) —
  deliberately deferred; plan Phase C4.

## Session log

- 2026-07-22: Cloned repo, read all planning + uploads, recorded GC rubric
  solution, onboarded structure, wrote implementation plan + intake doc.
- 2026-07-22 (later): precedence rule recorded; ADR-0001 (0–3 meets=max
  scale) decided and propagated to solution doc v2, plan, CLAUDE.md;
  20-item changes catalog extracted from planning notes.
