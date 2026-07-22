# Current Scope, Priorities, and Onboarding Readiness

## Current assessment

The repository now contains enough planning context for an advanced onboarding model to understand the core problem, the intended user workflow, the principal outputs, and the most important constraints.

The project is not fully specified, and it should not be. The current notes are intended to define the problem, goals, boundaries, source materials, and desired shape while leaving implementation choices to the model that performs the repository setup.

## Core purpose

The repository should support a teacher-facing system for processing existing instructional assignments individually or in batches.

The system should combine assignment-level analysis with repository-level memory so it can produce usable instructional artifacts and track standards coverage across time.

The main value is reducing repeated manual prompting, waiting, copying, and reconstruction across a large body of existing assignments.

## Primary classes and priority

The system should organize work by class rather than only by grade.

The principal classes are:

- 9th Grade College Prep
- 10th Grade College Prep
- 11th Grade College Prep

The initial priority is:

1. 10th Grade College Prep
2. 11th Grade College Prep
3. 9th Grade College Prep, deferred unless it becomes useful sooner

The system should not assume that materials, standards choices, rubric language, or expectations are identical across these classes even when standards frameworks overlap.

## School-year context

Assignments and derived artifacts may need a school-year indicator.

This would support later questions such as:

- Which assignments were used in a particular year?
- Which standards were covered during that year?
- How did an assignment or rubric change over time?
- Which materials belong to the current course version?

The exact year-based planning workflow is deferred. The initial structure should preserve enough metadata to add it later without forcing the system to schedule units or decide when assignments should be taught.

## Core inputs

The system should eventually accept:

- One assignment
- Several files belonging to one assignment
- A batch of loosely organized assignment files
- A folder hierarchy containing many assignments
- Existing Google Classroom template materials
- Rubric guidance and working spreadsheet files
- Teacher clarity and visual learning source documents
- Long source texts converted to Markdown for protected model access

The ingestion process should preserve folder structure when available and use AI-assisted grouping when files are loose or inconsistently named.

## Core outputs

For each assignment group, the primary output package should include:

- Teacher clarity model or artifact
- Standards alignment analysis
- Copy-ready standards list for Google Classroom
- Google Classroom-compatible rubric artifact
- Copy-ready Google Classroom title
- Copy-ready Google Classroom directions
- Visual learning package
- Teacher-review notes and uncertainties

The visual learning package is expected to include learning goals, success criteria, learning targets, an example prompt or task representation, what students do, and a progression of models from Advanced through No Evidence of Skill with explicit comparisons among adjacent levels.

## Standards registry

The repository should maintain longitudinal memory of standards use.

The registry should show:

- Which standards have been selected
- Which assignments support them
- How often they have appeared
- Whether they are primary, specific, supporting, contextual, or directly assessed
- Which strands or substandards remain underrepresented
- Parent-child relationships among standards

The registry should help make real coverage visible without attaching weak standards merely to complete a checklist.

## Grading philosophy

The standards rows and holistic rubric criterion serve different purposes.

The standards rows provide descriptor-based competency evidence and may be scored initially by Wayground AI with teacher review.

The holistic criterion carries most of the practical grade weight and remains primarily a teacher judgment.

Standards levels are ordinal descriptors rather than percentages. Full points on a standards row may mean that the student met expected competency, not that the work was perfect or exceptional.

For regular college-preparatory classes, meeting the standard should be sufficient for full ordinary credit. Exceeding the standard should not become a hidden requirement.

## Privacy and source-access boundary

The interface may be reachable through the web, but protected full texts and student exemplars must not become publicly accessible.

The processing agent may need authorized access to those materials.

Student exemplars must be anonymized and should receive an additional identifier check even when the teacher has already reviewed them.

The implementation may use protected hosted storage, temporary processing, the Mac Mini, or a hybrid arrangement. The present notes define the access boundary but do not prescribe the architecture.

## Additional desirable outputs

Some assignments lack answer keys. Others would benefit from clearer instructions, more scaffolding, or additional hints.

Possible later outputs include:

- Answer keys
- Teacher keys or expected-response guides
- Improved student directions
- Hints and scaffolds
- Revised prompts
- Additional examples
- Conversion of older RACE-based materials toward CER

These are valuable extensions but are not required to define the initial core.

## Deferred planning features

The following are intentionally deferred:

- Deciding when each assignment should be taught
- Building a complete course calendar or pacing guide
- Sequencing units across a school year
- Fully onboarding 9th grade materials
- Perfecting final visual formatting
- Automating every Google Classroom click
- Finalizing deployment architecture

The initial repository should avoid prematurely treating these as required first-version features.

## What the onboarding model should do

A strong onboarding model should be able to use the planning notes and uploaded authoritative files to:

1. Synthesize the requirements without replacing the teacher's definitions with generic ones.
2. Propose a repository structure that separates source materials, protected inputs, normalized assignment records, generated outputs, standards registry data, and application code.
3. Identify which requirements are settled and which remain open.
4. Create an implementation plan that supports batch processing first.
5. Preserve class and school-year metadata.
6. Keep the teacher in control of grouping, standards selection, rubric approval, grading overrides, and privacy decisions.
7. Avoid overengineering deferred planning or scheduling features.

## Remaining non-blocking questions

The following questions remain, but they do not prevent repository onboarding:

- Exact teacher clarity format
- Exact visual learning format
- Exact current rubric scale and wording
- Exact import and conversion workflow for Google Classroom rubrics
- Final storage and hosting architecture
- Exact source-file retention rules
- Exact standards hierarchy and registry schema
- Whether both parent and child standards should ever consume separate scored rows
- Which outputs should be generated in Markdown, spreadsheet, HTML, PDF, or Google-native formats

These should be resolved by analyzing the uploaded source documents, testing sample assignments, and refining the system iteratively.

## Readiness conclusion

The project is ready for an advanced model to perform an initial repository onboarding and propose a concrete first implementation.

The model should treat the current notes as a design brief, not as a rigid technical specification.

The most important first-version objective is a trustworthy batch workflow that groups assignment materials, produces the core output package, and updates a class-aware standards registry while preserving teacher review and protected source access.
