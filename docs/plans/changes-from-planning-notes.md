# Changes-to-Make — Planning Notes (TODAY) vs Uploaded Baseline (LAST TIME)

**Recorded by: Claude Fable 5**, 2026-07-22. Precedence rule: the
develop/planning/initial/ notes are Geoff's CURRENT intent and supersede
the user-uploads baseline wherever they diverge. This list extracts every
divergence/addition so none sits unactioned. Status column tracks landing.

| # | Change (planning-note source) | Supersedes in baseline | Status / lands in |
|---|------|------|------|
| 1 | **Remove scored Advanced level; 0–3 meets-=-max scale** (007 + direct instruction) | v01.08 0–4 scale | DONE — ADR-0001, solution doc v2 |
| 2 | **Eliminate +2/standard extra-credit offset** (007, consequence of #1) | v01.08 §9 offset | DONE — ADR-0001 |
| 3 | Advanced kept as ASPIRATIONAL tier in WAGOLL model progression + unscored recognition (007/011) | (new) | ADR-0001; build in WP C2.3 |
| 4 | Holistic completion-based DEFAULT descriptors + explicit anti-percentage language for Wayground (010) | template holistic wording | WP C2.2/C2.3 descriptor spec; solution doc v2 notes |
| 5 | Standards selection upgrade: anchor first, then strongest SPECIFIC substandard, parent-child rollup in registry without double-scoring (008) | v01.08 §1 (no substandard priority) | WP C2.1 spec |
| 6 | Reserved analytical attention for SL and L strands (008) | (absent) | WP C2.1 spec |
| 7 | Registry-aware selection: surface underrepresented standards as candidates, never as quota (008) | (absent — registry is new) | WP C2.1 + C2.5 |
| 8 | Longitudinal standards-coverage registry with role/evidence fields + teacher confirm/reject (008/012) | (absent) | WP C2.5 |
| 9 | Separate GC OPERATIONAL directions from full directions (Aeries parent-visible), infer teacher style, reuse existing wording when present (010/011) | (absent) | WP C2.4 |
| 10 | Copy-paste `CA CCSS:` block (already v01.07/08) retained; preserve teacher-approved order only (010) | consistent | WP C2.4 |
| 11 | Display-title vs filesystem-safe-name separation (pipes/emojis normalization) (011) | (absent) | WP C2.4 output naming |
| 12 | Citation philosophy in rubric language: good-faith locator attempt ≠ omission; AI-assisted quote-FINDING acceptable, original ANALYSIS protected (zero for outsourced analysis); similarity ≠ misconduct proof; evidence-after-claim formats recognized (010) | (absent from rubric descriptors) | WP C2.2 descriptor spec + C3.1 |
| 13 | Claim-evolution tolerance: claim/reasoning mismatch is graded as evolving thought vs no-analysis, not auto-failure (010) | (absent) | WP C2.2 descriptor spec |
| 14 | RACE→CER conversion direction for older materials, preserving intent (010/012) | RACE-based materials | backlog WP (C3.x extension) |
| 15 | AI-grading audit trail: proposed vs final levels + override rationale preserved (010) | (absent) | assignment.yaml schema (C2.x), C3.1 |
| 16 | Batch grouping with confidence tiers + teacher confirm/split/merge; folder structure as strong signal; GC templates folder as corpus (009) | (absent) | WP C1.2 (already planned; confidence-tier detail added) |
| 17 | Class-based org (10cp/11cp/9cp) + school-year metadata on all artifacts (012) | (absent) | landed in layout; enforce in schemas (C2.x) |
| 18 | Student-exemplar anonymization + three-state preflight (005) | (absent) | landed in CLAUDE.md rules; WP C0.3/C3.2 |
| 19 | Protected-source access boundary (web-reachable interface ≠ public texts) (004) | (absent) | landed in CLAUDE.md; governs C4 |
| 20 | xlsx authoritative / tsv derived rule (006) | tsv treated loosely | landed in solution doc gotcha #2 |

Rows marked "WP …" must appear in the corresponding work-package specs
before those WPs are delegated; this table is the checklist for that.
