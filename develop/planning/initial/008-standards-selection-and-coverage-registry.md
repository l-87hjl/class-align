# Standards Selection and Coverage Registry

## Why the existing one-assignment method is insufficient

The previous workflow asked ChatGPT to analyze each assignment independently and identify the most relevant standards for that assignment.

That is reasonable when the task is only to align one assignment at a time. It becomes incomplete when the broader goal is to demonstrate standards coverage across a course, grade level, unit sequence, or school year.

The repository therefore needs memory of prior selections and a visible registry of coverage.

The system should be able to answer questions such as:

- Which standards have been attached to assignments so far?
- How many times has each standard appeared?
- Which assignments provide evidence for each standard?
- Which standards are heavily represented?
- Which standards or substandards are absent or underrepresented?
- Are some domains being overlooked because they are less obvious in assignment directions?

The registry is partly an instructional planning tool and partly a documentation tool. It should help demonstrate visibly that the course addresses the required standards, not merely assume that coverage is implicit.

## Assignment-level selection still needs to be defensible

The registry should not cause the system to attach arbitrary standards merely to fill gaps.

Every selected standard should remain supportable from the actual assignment, its expected student work, its instructional context, or a clearly identified classroom activity.

The system should distinguish between:

- A standard that is central and directly assessed
- A standard that is specifically demonstrated by one part of the task
- A supporting standard that is meaningfully present
- A standard that is plausible only because of unstated classroom practice
- A standard being considered primarily because it is underrepresented elsewhere

Coverage balancing should influence what the system notices and investigates. It should not override honest alignment.

## Proposed selection priorities

When enough valid standards are available, selection should consider the following priorities.

### 1. Strongest direct standard

The first priority is the standard that best captures what the assignment is mainly about.

This should be the clearest, most defensible alignment and the standard most visible in the required student performance.

### 2. Strongest specific substandard

At least one slot should be used for the strongest applicable specific standard or substandard when the standards framework contains subdivisions.

For example, if a broad writing standard has lettered or numbered components, the most directly relevant component should be surfaced rather than recording only the parent standard.

The purpose is to prevent the registry from claiming broad coverage while repeatedly assessing only one narrow component.

### 3. Parent-standard relationship

The system should retain the relationship between a specific substandard and its parent standard.

Whether both should consume separate Google Classroom learning-goal slots is not yet settled.

Possible approaches include:

- Tagging both the parent and the specific substandard
- Tagging only the specific substandard while allowing the registry to roll it up automatically to the parent
- Tagging the parent only when the assignment genuinely addresses multiple components of it

The registry should support parent-level reporting even when only a specific descendant is attached to the assignment. This may avoid spending two grading slots on substantially overlapping evidence.

## Avoiding double counting

A parent standard and one of its substandards may describe overlapping evidence.

If both appear as separately scored rubric rows, the same student performance could be graded twice. That may distort the grade and consume limited standards slots.

The system should therefore distinguish between:

- Reporting coverage at both parent and child levels
- Scoring the same evidence twice

A likely long-term design is to allow one scored specific standard to count toward the parent standard in the coverage registry without requiring a second scored criterion. This remains a planning hypothesis to test against the actual standards framework and Google Classroom behavior.

## Supporting standards and less-visible domains

After the strongest direct and specific standards are identified, the remaining available slots should be used for other genuinely supported standards.

The system should make a deliberate effort to inspect domains that independent assignment analysis tends to underrepresent, especially:

- Speaking and listening
- Language, grammar, usage, conventions, vocabulary, and style

These domains often appear through classroom practice or recurring expectations rather than through a lesson devoted entirely to one isolated standard.

For example:

- An assignment may include group discussion even when the written prompt does not fully describe how discussion will be conducted
- Transitions, grammar, citation practices, and language choices may be taught incrementally across many assignments rather than in one standalone lesson

The system should surface these standards when there is meaningful evidence for them, rather than allowing them to disappear merely because reading and writing standards are more obvious to a model.

## Reserved attention, not automatic reserved scoring

It may be useful to reserve analytical attention for certain domains, but that does not necessarily mean reserving a scored rubric slot regardless of relevance.

A practical analysis process could ask explicitly:

1. Is there a directly assessed speaking and listening component?
2. Is there a directly assessed language or conventions component?
3. Is the evidence visible in the assignment itself?
4. Is the evidence present only in teacher-described classroom practice?
5. Would adding the standard clarify real coverage, or merely improve the appearance of balance?

This helps the system notice valid but less-obvious standards without fabricating alignment.

## Registry fields

The eventual standards registry may need to preserve more than a simple checked or unchecked state.

Useful fields may include:

- Standard identifier
- Full standard text
- Parent standard identifier
- Domain or strand
- Grade level or course
- Assignment identifier and title
- Unit or sequence
- Date or school year
- Alignment role: primary, specific, supporting, contextual, or provisional
- Whether the standard is directly assessed
- Whether it appears as a scored rubric criterion
- Evidence or rationale for selection
- Number of prior appearances
- Teacher confirmation, revision, or rejection

This would allow the system to report coverage honestly at several levels of detail.

## Visibility and accountability objective

One purpose of the system is to help make standards coverage visible to people who expect lesson, assignment, rubric, and standards documentation to connect clearly.

The teacher's actual instructional planning does not necessarily proceed as one isolated lesson per standard. Skills may be introduced, revisited, practiced, and assessed incrementally across many assignments.

The registry should make that reality legible without falsely simplifying it.

It should support statements such as:

- This standard is introduced here and assessed more fully later
- This language skill recurs across several assignments
- This substandard has been directly assessed three times
- This parent standard appears broadly covered, but one component remains thin
- Speaking and listening occurred in the classroom process even though the final product was written

## Use of the 10 available learning-goal slots

Because Google Classroom permits up to 10 learning goals on a classwork item, the system has room to represent more than only the most obvious reading or writing standards.

A provisional selection pattern may be:

1. Strongest direct standard
2. Strongest specific substandard
3. Additional directly assessed standards
4. Meaningful supporting standards
5. A speaking and listening standard when genuinely applicable
6. A language standard when genuinely applicable
7. Other underrepresented but defensible standards identified through registry context

This is a prioritization framework, not a quota. An assignment should use fewer than 10 standards when fewer than 10 are genuinely supported.

## Teacher review

The system should propose standards with reasons and registry context, but the teacher should control the final selection.

The review experience should make it easy to see:

- Why each standard was proposed
- Whether it is primary, specific, or supporting
- How often it has already been used
- Which related standards remain underrepresented
- Whether the proposal depends on classroom activity not visible in the uploaded assignment
- Whether selecting both a parent and child standard would duplicate scoring

## Open questions

- Which standards framework and hierarchy will be used?
- Does Google Classroom permit both parent and substandard learning goals as distinct tagged items?
- Should a tagged substandard automatically count as parent-standard coverage in the registry?
- When, if ever, should both parent and child appear as scored rubric rows?
- How should repeated exposure differ from direct assessment in coverage reports?
- How should oral discussion or collaborative work be documented when it is not explicit in the assignment file?
- Should language standards be attached to many assignments as recurring expectations, or only when explicitly assessed?
- How should the system identify meaningful coverage without optimizing merely for a visually complete checklist?
- What level of evidence would be persuasive to district reviewers or future automated audits?
