# Batch Ingestion and Assignment Grouping

## Expected input pattern

A central user-facing capability is batch upload of existing instructional materials.

An assignment may consist of more than one document, such as:

- Student directions
- A prompt or task sheet
- A source text or excerpt
- A planning organizer
- A model or exemplar
- A rubric
- A presentation or supporting handout
- Teacher-facing notes

The system therefore cannot assume that every uploaded file represents a separate assignment.

## Similar naming as a useful but imperfect signal

The teacher generally tries to give related assignment files similar names, but naming consistency cannot be guaranteed.

The ingestion process should use filenames as one signal among several rather than as the sole grouping rule.

Potential grouping signals may include:

- Similar filename stems
- Shared assignment titles inside the documents
- Repeated unit, text, author, chapter, or topic names
- References from one document to another
- Matching due-date, course, or grade-level language
- Shared rubric terminology
- Similar creation or modification context
- Common folder ancestry when folders are present
- Document roles that naturally complement one another, such as directions plus organizer plus rubric

## AI-assisted grouping

For a loose batch of files, the system should propose which documents likely belong to the same assignment.

It should not silently merge files with uncertain relationships. A useful grouping result would distinguish among:

- High-confidence assignment groups
- Probable groups requiring review
- Files that may belong to more than one assignment
- Files whose assignment relationship is unclear
- Reusable materials that may support several assignments

The teacher should be able to confirm, split, merge, or rename proposed groups before downstream standards and rubric processing.

## Folder-aware ingestion

When the teacher provides folders, directory structure should be treated as a strong organizational signal.

A folder named for an assignment may contain all of the documents associated with that assignment. Nested folders may preserve useful context such as:

- Course
- Grade level
- School year
- Unit
- Assignment
- Supporting resources

The system should preserve that structure during ingestion rather than flattening it unnecessarily.

Folders should improve grouping confidence but should not make the system ignore contradictory evidence inside the documents.

## Google Classroom templates folder as a possible corpus

A promising source may be the templates folder associated with a previous Google Classroom course.

The apparent advantage is that template copies may represent the original assignment materials before student-specific copies or submissions were created. The folder and subfolder structure may already compartmentalize documents by assignment name, making batch processing substantially easier.

A full templates directory could potentially provide:

- Assignment-level folders
- Related documents already grouped together
- Original teacher-authored versions
- A large existing body of 9th-, 10th-, and 11th-grade materials
- A natural hierarchy for initial repository or local processing

This source should be inspected before being treated as automatically safe. The teacher expects template files not to contain student information, but the ingestion workflow should still check for names, comments, sharing metadata, revision history, or other identifiers.

## Possible transfer and processing paths

The templates folder or another assignment corpus might be:

- Copied to the Mac Mini and processed locally
- Added to a private or otherwise protected GitHub repository
- Uploaded through the eventual web interface
- Processed from another protected storage location while only derived metadata is committed to Git

The final choice should consider privacy, copyright, file size, convenience, and the need to avoid repetitive copying and pasting.

## Desired batch output

After ingestion and grouping, each assignment should have a coherent processing unit that can support later work such as:

- Identifying the primary assignment directions
- Identifying supporting files and source texts
- Detecting an existing rubric or model
- Determining course, grade, unit, and assignment context
- Proposing standards
- Generating or revising the rubric
- Applying teacher clarity and visual learning procedures
- Updating the longitudinal standards registry

The grouping step should occur before those analyses so that the model evaluates the complete assignment rather than an isolated file whenever possible.

## Provenance and confidence

The system should retain how an assignment group was formed.

Useful metadata may include:

- Original path
- Original filename
- Proposed assignment title
- Grouping confidence
- Signals used to group the files
- Teacher confirmation status
- Whether the group came from an existing folder or AI inference
- Any files excluded or left unresolved

This makes it possible to correct the organization later without losing the source relationships.

## Current direction

The strongest likely starting point is to obtain an existing Google Classroom templates folder with its subdirectories intact, inspect it for privacy issues, and use the directory structure as the initial assignment grouping.

The system should nevertheless retain a fallback capability for batches of loosely organized files, since clean folder organization cannot always be assumed.

## Open questions

- How can the templates folder be exported or copied while preserving its hierarchy?
- Which file types occur in that folder?
- Do Google Docs arrive as links, native files, or exported documents?
- Are assignment titles consistently represented in folder names?
- Does the folder include reusable resources shared across several assignments?
- What privacy and metadata checks are needed before ingestion?
- Should source assignment files live in Git, private object storage, or only on the Mac Mini?
- How should duplicate assignments from different years or course sections be recognized?
- Should the teacher approve assignment groups before any model processing begins?
