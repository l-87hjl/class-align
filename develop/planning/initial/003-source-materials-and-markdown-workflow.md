# Source Materials and Markdown Workflow

## Expected source files

The project will receive several existing files that define or support the current workflow. Based on the present working set, these include materials such as:

- `GC_Rubric_Directions_CURRENT_v01.08.md`
- `GC_Rubric_Template_STRUCTURE.md`
- `GC_Rubric_Template_WORKING.xlsx`

These files are expected to provide the operative instructions, structural expectations, and working rubric format used for Google Classroom-related processing.

They should be treated as source materials to analyze and preserve, not casually rewritten or replaced with generic alternatives.

## Assignment and text inputs

The project will not necessarily store every full text as a permanent repository artifact.

For assignment-specific work, full texts may be converted into Markdown so they can be parsed efficiently by a model. This is especially useful when a request depends on the actual text, such as:

- Standards or assignment alignment
- Teacher clarity review
- Visual learning review
- Rubric generation tied to a specific work
- Evidence-based analysis of an assignment or reading

The Markdown conversion is intended to make long source material easier to process within model context and token limits.

## Purpose of the conversion workflow

The important design principle is that source texts should be prepared in a form that supports reliable, bounded analysis without requiring repeated manual restructuring.

Markdown is currently preferred because it:

- Is easy for models to parse
- Preserves headings, sections, pagination cues, and other useful structure
- Is portable across tools and environments
- Can be versioned when appropriate
- Is easier to divide into chunks than many original document formats
- Reduces friction when the same text supports several kinds of instructional analysis

## Distinction between reusable guidance and temporary content

The repository may need to distinguish between two kinds of material:

### Reusable workflow guidance

Examples include rubric directions, rubric structure definitions, standards-identification procedures, teacher clarity definitions, and visual learning procedures.

These materials define how the system should interpret and process instructional work over time.

### Assignment-specific source content

Examples include a novel, article, worksheet, prompt, or other text being used for one or more assignment-processing tasks.

These materials may be uploaded, converted, processed, and then retained or discarded according to later repository and storage decisions.

## Implications for the eventual interface

The future interface may need to support:

- Uploading original source files
- Accepting already-converted Markdown
- Converting supported document formats into structured Markdown
- Preserving pagination or section markers when they matter
- Associating source texts with one or more assignments
- Reusing one converted text across multiple alignment, clarity, visual learning, or rubric requests
- Handling long texts in chunks without losing the relationship to the whole work

The exact conversion and storage method remains open.

## Current boundary

The immediate planning goal is to establish that Markdown conversion is part of the teacher's existing preparation workflow and is important for model usability.

This note does not yet specify:

- Which file-conversion tools must be used
- Whether converted texts belong in Git, object storage, a database, or temporary processing space
- How chunking should be implemented
- Whether copyrighted full texts should ever be stored in a public repository
- How long uploaded or converted source material should be retained

Those decisions should be made later with the actual files, access model, copyright constraints, and deployment environment in view.
