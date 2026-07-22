# Assignment Outputs and Human-in-the-Loop Grading

## Desired per-assignment output package

After an assignment or assignment group is processed, the system should return a practical package the teacher can use in Google Classroom and the surrounding workflow.

The likely package includes:

- Teacher clarity materials required by the teacher's established procedure
- Visual learning materials or checks required by the corresponding framework
- A completed Google Classroom rubric in spreadsheet form
- A concise standards list suitable for copying and pasting
- Proposed Google Classroom-facing assignment instructions
- Processing notes, uncertainties, and items requiring teacher review

The exact contents should be refined after the authoritative teacher clarity, visual learning, and rubric-direction files are analyzed.

## Standards copy-and-paste block

One output should be a short, clean standards block that can be pasted into the Google Classroom assignment description.

A provisional form might look like:

```text
California CCSS: [standard identifiers]
```

This is intended to reduce the friction of manually locating the selected standards while tagging the classwork item and connecting standards to rubric criteria.

The standards block should preserve the final teacher-approved order and identifiers. It should not include speculative or rejected standards.

## Google Classroom-facing instructions

The teacher's full assignment directions and the instructions entered into Google Classroom may serve different purposes.

The Google Classroom version may need to emphasize concise operational information, such as:

- What students must submit
- Where or how to complete the work
- Required attachments or document format
- How to turn it in
- Essential due-date or completion information

These instructions are important because the Google Classroom description may be the version surfaced to parents through the connected student-information system, currently Aeries.

The system should therefore distinguish among:

- Full instructional directions
- Student-facing task directions
- Google Classroom operational instructions
- Parent-visible summary language

The existing Google Classroom template corpus may or may not preserve these descriptions. The system should detect and reuse them when present, and propose them when absent.

## Batch-processing value

The first version does not need to eliminate every manual Google Classroom step.

Substantial value comes from processing many assignments at once and returning usable artifacts without repeated prompting, model startup, and copying between individual chats.

The teacher may still need to perform steps such as:

- Opening each generated rubric
- Converting or saving it into the Google-native format required by the current workflow
- Importing the rubric into Google Classroom
- Looking up and tagging each standard
- Connecting each tagged standard to the appropriate rubric criterion

These remaining minutes of manual work per assignment are acceptable if the system removes the much larger burden of creating every artifact separately.

The exact Google Classroom import requirements should be verified later against the current platform and the supplied rubric-direction files.

## Role of Wayground AI in grading

The teacher currently uses the AI grading capability formerly associated with Quizizz and now provided through Wayground.

It is especially useful for standards-based rubric rows because it can reduce repeated micro-decisions across many criteria.

Useful functions include:

- Selecting a performance level for each standards criterion
- Applying or transferring those selections into the Google Classroom rubric workflow
- Providing a first-pass standards judgment that the teacher can review and override

This assistance is valuable because deciding repeatedly between adjacent levels across many standards criteria is time-consuming even when the teacher retains final authority.

## Human judgment remains central

The teacher should remain the final decision-maker for all rubric results.

This is especially important for the holistic criterion, which carries most of the assignment's practical grade weight and reflects an integrated judgment of the work as a whole.

The automated evaluator may be useful as a signal, but it should not control the holistic score.

## Holistic scoring tendency to correct

The current AI grader often appears to score the holistic row one or two levels below the teacher's likely judgment.

A probable cause is that it treats the rubric level as a conventional percentage scale. It may reason that work resembling an ordinary `C` should receive roughly 70 percent of the available holistic points.

That interpretation conflicts with the teacher's grading design when the holistic row is primarily completion-based.

The system should therefore describe the holistic levels explicitly and avoid relying on point fractions to communicate their meaning.

## Completion-based holistic default

For many existing assignments, the default holistic question is approximately:

> Did the student complete the assignment in good faith, follow the directions, and include the required parts?

The holistic evaluation may consider:

- Whether all major parts were attempted
- Whether the student followed the required format
- Whether the response addresses the task
- Whether quotations or textual evidence were included when required
- Whether the student made a reasonable attempt at citation
- Whether the analysis reflects the student's own thinking
- Whether the submission functions as a complete response even if it is not polished or advanced

Not every assignment will use a purely completion-based holistic criterion. The system should treat this as a common default that can be overridden by assignment-specific expectations.

## Citation and textual-evidence expectations

When an assignment requires textual evidence, the teacher expects students to provide an actual quotation from the assigned work.

A good-faith citation attempt normally includes:

- The author's last name when appropriate
- A page number when available
- A paragraph number when that is the usable locator
- A line number for poetry or another line-based text
- Another reasonable locator suited to the source format

Perfect citation formatting is not always the central issue. The important distinction is whether the student made a real attempt to identify and locate the evidence.

Simply omitting the citation or evidence is materially different from making an imperfect but recognizable attempt.

## Evidence may support a preceding statement

Some assignment formats may ask students to state what a quotation demonstrates and then place the supporting quotation after a colon, sometimes in parentheses.

The rubric and grading instructions should recognize the intended relationship between the student's statement and the quoted evidence rather than requiring only one rigid sentence pattern.

## Ethical use of AI for locating quotations

Using AI or another search aid to help locate a real quotation from the assigned text is not automatically considered improper in this grading philosophy.

The important requirements are that:

- The quotation actually appears in the assigned source
- The student uses it accurately
- The student provides a reasonable citation or locator
- The student's analysis remains their own

The system should not treat assistance in finding evidence as equivalent to outsourcing the student's thinking.

## Boundary around original analysis

The student's analytical reasoning is the part of the response where independent thought is most important.

In the teacher's present approach, AI-generated or plagiarized analysis can justify a zero on the assignment because the analysis is the core intellectual work being assessed.

Other parts of a structured response may naturally overlap across students:

- Restating the question
- Making a broad claim such as agree or disagree
- Selecting the same useful quotation
- Using a required response format

Those similarities do not necessarily demonstrate misconduct.

The analysis or reasoning section must explain the evidence in the student's own words and show the student's thinking.

Any eventual automated support in this area should produce evidence for teacher review rather than making irreversible misconduct determinations on its own.

## RACE and CER transition

Some current assignments use the RACE structure:

- Restate
- Answer
- Cite
- Explain

The teacher expects to move toward CER:

- Claim
- Evidence
- Reasoning

The substantive concern remains similar: the reasoning or explanation is where the student connects the evidence to the claim and demonstrates original analysis.

When converting materials from RACE to CER, the system should preserve the teacher's actual instructional intent rather than mechanically renaming labels.

## Claims may evolve during thinking

Students may write an initial claim before locating evidence and then develop a different or more nuanced understanding during analysis.

This can create imperfect alignment among the opening claim, topic sentence, evidence, and final reasoning.

The teacher may still value the work because the change can show genuine thinking, even when the student does not yet have the metacognitive or revision skill to return and update the earlier structure.

The rubric should not automatically treat every claim-analysis mismatch as a total failure. It should distinguish among:

- A structural inconsistency that needs revision
- Reasoning that genuinely does not support the claim
- Evidence of evolving thought
- A response with no meaningful analysis

## Implications for generated rubrics

Rubrics intended for Wayground-assisted grading should include descriptors clear enough to prevent percentage-based reinterpretation.

They may need to state explicitly that:

- `Meets` represents successful expected competency
- Full points on a completion-based holistic level do not mean exceptional mastery
- Good-faith completion and inclusion of required parts carry substantial weight
- Citation attempts should be evaluated differently from total omission
- Evidence selection and original analysis are distinct criteria or considerations
- Similar claims or quotations are not, by themselves, proof of improper AI use
- Original reasoning is the protected core of the student's work

## Human review and audit trail

The eventual workflow should preserve:

- The AI-proposed standards levels
- The teacher's final standards levels
- The AI-proposed holistic level, if generated
- The teacher's final holistic judgment
- Any teacher override and optional rationale
- Flags concerning missing evidence, missing citation, or questionable analysis

This could help improve future rubric language and reveal where automated grading repeatedly differs from the teacher's intended philosophy.

## Open questions

- What exact output files should be generated for every assignment?
- What format should the copy-and-paste standards block use?
- Can Google Classroom-facing instructions be recovered from the template export?
- What Google-native conversion steps can or cannot be automated?
- What is the third Wayground benefit the teacher had in mind but did not fully specify in this note?
- Which assignments should default to completion-based holistic scoring?
- How should citation attempts be described at each rubric level?
- How should the system flag suspected AI-generated analysis without overclaiming certainty?
- Which school or district academic-integrity policies must constrain the eventual workflow?
- How should RACE-to-CER conversion affect existing assignments, exemplars, and rubric language?
