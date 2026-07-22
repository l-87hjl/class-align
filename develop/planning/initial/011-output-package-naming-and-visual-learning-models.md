# Output Package, Naming, and Visual Learning Models

## Core input-to-output idea

The system should accept either:

- One assignment
- Several assignment-related documents
- A batch of assignments
- A folder tree containing many assignments

For each confirmed assignment group, it should return a practical, copy-ready set of outputs rather than only an analysis narrative.

The first versions do not need perfect final formatting. Correct content and a usable structure matter first; presentation can be refined later.

## Expected assignment output bundle

Each processed assignment should eventually produce some version of the following:

1. Teacher clarity model
2. Standards alignment
3. Google Classroom rubric
4. Google Classroom assignment title
5. Google Classroom directions
6. Visual learning package
7. Notes requiring teacher review

These outputs should remain connected to the same assignment record so they are easy to review and use together.

## Teacher clarity model

The system should generate the teacher clarity artifact defined by the authoritative teacher clarity source documents.

The exact fields, wording, and formatting should come from those documents rather than from a generic interpretation of teacher clarity.

The desired result is a usable artifact that the teacher can place with or alongside the assignment.

## Standards alignment

The standards output should include:

- The strongest direct standard
- The strongest applicable specific substandard
- Other defensible supporting standards
- Registry context when useful
- A short copy-and-paste standards line for Google Classroom

The system should retain the difference between analysis detail and the concise text the teacher actually needs during setup.

## Google Classroom rubric

The rubric output should follow the supplied Google Classroom rubric directions and working template.

It should be generated in a spreadsheet format suitable for the teacher's current import and conversion workflow.

The system should preserve:

- The holistic criterion
- Standards-linked criteria
- Correct point structure
- Performance-level descriptors
- Any required standards-to-criterion relationship information

## Google Classroom title

The teacher uses a recognizable naming style for Google Classroom assignments.

The system should infer that style from the existing assignment corpus rather than requiring the entire naming convention to be described abstractly in advance.

The output should include a copy-ready title.

### Naming normalization

Existing titles may include:

- Long descriptive names
- Emojis
- Vertical bars or pipe characters (`|`)
- Other punctuation accepted by Google Drive but handled inconsistently by Microsoft tools, downloaded archives, operating systems, GitHub paths, or conversion utilities

The system may normalize filenames or exported artifact names when necessary for compatibility.

Acceptable cleanup may include:

- Replacing `|` with ` - `
- Removing unsupported filesystem characters
- Simplifying repeated whitespace
- Preserving meaningful ordering and distinctions
- Retaining emojis when they survive the workflow reliably
- Removing or replacing emojis when they cause conversion, path, or processing problems

The original display title and the filesystem-safe name should be stored separately when they differ.

For example:

```text
Display title: Unit 3 | Literary Analysis 📚
Safe filename: Unit 3 - Literary Analysis
```

Normalization should not erase distinctions that help the teacher identify course, unit, text, assignment type, or sequence.

## Google Classroom directions

The output should include copy-ready Google Classroom directions.

These may be shorter and more operational than the full assignment instructions.

They may include:

- What students are completing
- Which document or attachment to use
- Whether they should type directly into a template
- What must be submitted
- How to turn it in
- Any essential citation or formatting reminder

The system should infer the teacher's typical style from prior assignments and preserve existing wording when a usable Google Classroom description is available.

## Visual learning package

The system should produce the visual learning materials defined by the authoritative visual learning documents.

The expected package appears to include at least:

- Learning goals
- Success criteria
- Learning targets
- An example prompt
- A description of what students do
- Models or exemplars across a progression of performance
- Explanations of the differences between adjacent levels

The source documents should determine the final labels and exact formatting.

## What a good one looks like

The visual learning framework includes the idea commonly described as "what a good one looks like," often abbreviated as WAGOLL.

The system should not provide only one successful model. It should help make quality visible through a progression of examples and explicit comparison among levels.

The expected performance sequence is:

1. Advanced
2. Proficient
3. Progressing
4. Developing
5. No Evidence of Skill

These may be teacher-created models initially and may later include approved anonymized student exemplars.

## Required explanation by level

The model package should not merely label examples. It should explain what changes from one level to the next.

### Advanced

The advanced model should explain:

- How it exceeds the standard
- What makes it stronger than the proficient model

### Proficient

The proficient model should explain:

- How it meets the standard
- Why it is not advanced
- How it improves on the progressing model

### Progressing

The progressing model should explain:

- Why it does not yet meet the proficient level
- How it improves on the developing model

### Developing

The developing model should explain:

- How it differs from the progressing model
- How it improves on no evidence of skill

### No Evidence of Skill

The no-evidence model should explain:

- What is missing
- How the developing model begins to demonstrate the skill beyond this level

## Comparison structure

The system should make the progression legible in both directions:

- What must improve to move upward
- What has been lost when moving downward
- Which success criterion changes
- Which parts remain constant
- Whether the difference is completeness, accuracy, reasoning, evidence, control, sophistication, or another assignment-specific quality

The explanations should be concrete and tied to the actual assignment rather than relying on vague phrases such as "more detail" or "better analysis."

## Models and standards

The exemplar ladder should align with the rubric and standards language.

In particular:

- Proficient should visibly represent meeting the expected standard
- Advanced should show a genuine extension beyond proficiency
- Progressing should show partial but meaningful evidence
- Developing should show emerging or inconsistent evidence
- No Evidence of Skill should show that the relevant skill is absent, inaccessible, or not demonstrated in the submitted response

The point values assigned in Google Classroom should not cause these qualitative meanings to be reinterpreted as percentages.

## Assignment-specific generation

The models should be based on the actual assignment prompt, expected response, source material, and success criteria.

A generic model may not be useful if it does not resemble what students are actually being asked to produce.

The system may need to generate:

- A full sample response
- A partial response focused on one skill
- Annotated excerpts
- Side-by-side versions
- A progression built from the same underlying prompt

The final form should follow the supplied visual learning procedure.

## Copy-ready presentation

The interface should make it easy to copy individual outputs without selecting unrelated explanatory text.

Useful separate fields or download artifacts may include:

- Copy Google Classroom title
- Copy Google Classroom directions
- Copy standards line
- Download rubric spreadsheet
- Download or copy teacher clarity model
- Download or copy visual learning package

This is a usability requirement, not merely a formatting preference. The point is to reduce repeated manual assembly across many assignments.

## Teacher review

All generated outputs should be reviewable before final use.

The system should visibly mark:

- Inferred assignment names
- Reconstructed Google Classroom directions
- Standards with weaker or contextual evidence
- Models generated without an existing teacher or student exemplar
- Naming characters that were normalized
- Missing source information
- Any conflict among the assignment, rubric, clarity model, and visual learning package

## Open questions

- What is the exact teacher clarity output structure?
- What is the exact visual learning document structure?
- Is WAGOLL the preferred term in the supplied framework?
- Should the five performance models be full responses or focused excerpts?
- Should all five models always be generated, or may some be omitted for certain assignments?
- Should the Google Classroom title and local filename always be separate fields?
- Which emojis and punctuation should be preserved in display titles?
- Can existing Google Classroom directions be recovered from exported templates?
- Which outputs should be Markdown, spreadsheet, Google-native, PDF, or HTML?
- Should the interface provide one combined assignment package as well as individually copyable fields?
