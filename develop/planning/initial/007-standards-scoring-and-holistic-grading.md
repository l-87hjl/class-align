# Standards Scoring and Holistic Grading

## Purpose of this note

The rubric design needs to preserve an important distinction between:

- Standards-based evidence about a student's level of competency
- The holistic judgment that determines most of the assignment grade

The current numerical labels and exact Google Classroom limits still need to be verified against the source files. The concepts below are more important than the presently remembered numbers.

## Google Classroom rubric constraint

Google Classroom imposes a limit on the number of rubric criteria or available slots. The exact limit should be confirmed from the existing directions file rather than inferred from memory.

Within that limited structure, one criterion or slot is reserved for a holistic component reflecting the teacher's broader grading philosophy.

The remaining criteria may represent standards assessed by the assignment.

## Holistic criterion

The holistic component carries most of the practical grading weight.

It represents the teacher's overall professional judgment of the submitted work, including considerations such as:

- Whether the student followed the assignment directions in good faith
- Whether the work functions successfully as a whole
- Whether required elements are present
- Whether evidence and citations are handled correctly or reasonably correctly
- Whether the response demonstrates an appropriate overall level of care, completeness, and competence
- Other assignment-specific expectations that are not well represented by isolated standards rows

This is not intended to be an arbitrary impression. It is an integrated assessment of the whole performance, guided by the assignment directions, rubric language, models, and the teacher's established philosophy.

## Standards criteria

Standards rows provide evidence about how the student performed relative to particular competencies.

They are useful for:

- Showing alignment between the assignment and standards
- Giving students more specific information about strengths and needs
- Supporting automated or AI-assisted rubric evaluation
- Allowing the teacher to review, accept, revise, or disagree with an automated judgment
- Tracking standards coverage and performance over time

They are not intended to dominate the assignment grade in the regular college-preparatory classroom.

## The scale is ordinal, not percentage-based

A standards score must not be interpreted as a percentage merely because it uses numbers.

For example, if the operative scale eventually uses levels such as 1 through 3 or 1 through 4, the highest required competency level may be labeled `Meets the Standard` even when it receives all available points for that row.

Receiving 3 out of 3 points on a standards criterion would mean:

> The student demonstrated the expected basic competency for this course and assignment.

It would not mean:

> The work is perfect, exceptional, or equivalent to 100 percent mastery in an absolute sense.

Likewise, a lower level must not be calculated as a simple fraction of mastery. A score of 1 on a three-level scale does not inherently mean the student met one-third of the standard.

The numbers are labels and point values attached to qualitatively defined performance levels. The written descriptors control their meaning.

## Meets versus exceeds

For regular college-preparatory classes, `Meets the Standard` is the expected successful outcome.

Students should be able to complete solid, competent work and receive the full intended course credit without being required to perform at an advanced or `Exceeds` level.

An `Exceeds` level may still be valuable because it:

- Recognizes genuinely advanced performance
- Communicates what stronger or more sophisticated work looks like
- Preserves room for distinction
- May support other course levels or future uses of the same rubric

However, it should not function as a hidden requirement for earning full ordinary credit in the CP classroom.

## Current compensation workaround

The existing approach has sometimes retained an `Exceeds` point level while compensating students so they are not penalized for merely meeting the standards.

For example, if eight standards each contain one or two points above the `Meets` level, the teacher may award the corresponding eight or sixteen points as extra credit or an offset. This prevents the nominally unavailable advanced points from lowering a competent student's grade.

This can preserve fairness, especially on assignments worth 50, 100, or 200 points, but it creates administrative complexity and makes it easier to lose track of adjustments across assignments.

It may also become disproportionately significant on smaller assignments.

## Simpler alternative under consideration

A more sustainable approach may be to cap each standards row at `Meets the Standard` for the regular CP grading calculation.

Under that model:

- Meeting the standard earns the full available points for that criterion
- Students are not penalized for failing to exceed the expected course level
- No compensating extra-credit calculation is required
- Advanced performance can still be reflected in written feedback, a separate non-penalizing marker, or another rubric design if appropriate

This is currently a design direction under consideration, not yet a settled rule.

## Automated grading boundary

An automated evaluator such as Wayground may generate standards-based rubric judgments, but the teacher must remain able to review and override those judgments.

The system must be instructed explicitly that:

- Standards levels are descriptor-based categories
- Point totals do not define proportional mastery
- `Meets` can represent full successful performance for the course
- `Exceeds` is not automatically required for full ordinary credit
- The holistic criterion carries most of the intended grade weight
- The teacher's final judgment controls

## Design implications

The eventual system should avoid treating rubric cells as interchangeable arithmetic values without reading their descriptors.

It may need to preserve separately:

- The level label
- The written performance descriptor
- The point value used by Google Classroom
- Whether the level is required, optional, advanced, or non-penalizing
- The weight or role of the holistic criterion
- The teacher's final override

This separation will help prevent an AI or import process from confusing a complete point award with exceptional performance.

## Items to verify later

- The exact Google Classroom maximum for rubric criteria or standards slots
- The exact current standards scale and its numeric values
- Whether the existing rubric uses three or four performance levels
- The current names and wording of each level
- How the holistic criterion is represented in the working spreadsheet
- Whether Google Classroom permits a non-scoring or extra-credit `Exceeds` indicator
- Whether different course levels should use different scoring treatments
- Whether the preferred long-term approach is to remove compensating points and make `Meets` the standards-row maximum
