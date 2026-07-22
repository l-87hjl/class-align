# Rubric Spreadsheet Formats

## Working source

The teacher will provide the working rubric in `.xlsx` format.

This should be treated as the authoritative editable version when it contains structure that may not survive a flat export, including:

- Multiple worksheets
- Formulas
- Cell relationships
- Merged cells
- Formatting used to communicate rubric structure
- Validation or dropdown fields
- Hidden reference sheets or supporting data

Modern tooling can read `.xlsx` files directly, so the format does not prevent machine processing.

## Alternative export formats

The same rubric can also be exported as:

- HTML
- CSV
- TSV
- ODS

Each format serves a different purpose.

### TSV

TSV is likely the easiest flat-text representation for model and programmatic processing when the relevant rubric is a single rectangular table.

It has several advantages:

- Simple text parsing
- Clear row-and-column boundaries
- Better tolerance than CSV for rubric descriptions containing commas
- Easy inspection and version comparison
- Low processing overhead

Its main limitation is that it does not preserve spreadsheet formatting, formulas, merged cells, or multiple-sheet relationships.

### CSV

CSV is similarly easy to process, but rubric language often contains commas, which increases quoting and escaping complexity.

It remains useful when required by another system or when the data is simple and consistently exported.

### HTML

HTML may preserve more of the visible table layout than CSV or TSV, including some merged-cell and presentation structure.

It can be useful as a secondary reference for how the rubric is meant to look, but generated spreadsheet HTML may contain substantial presentation markup and is usually less convenient as the primary machine-readable source.

### ODS

ODS is an open spreadsheet format and can preserve workbook structure more fully than CSV or TSV.

However, support across automation libraries and hosted processing environments is generally less uniform than support for `.xlsx`. It is not automatically the easiest format merely because it is open.

## Current preferred approach

The strongest working arrangement is likely:

1. Keep the `.xlsx` file as the authoritative working source.
2. Export the principal rubric sheet as `.tsv` for simple, reliable machine parsing.
3. Optionally retain an HTML export when the visual table arrangement is important to interpret.

This gives the system both the complete workbook and a simplified interchange representation.

The system should not assume that the TSV export contains every meaningful feature of the workbook. When discrepancies arise, the `.xlsx` source should control unless the teacher explicitly designates another format as authoritative.

## Implications for the eventual system

The future workflow may need to:

- Read `.xlsx` directly
- Identify the relevant worksheet or worksheets
- Produce or accept a TSV representation for downstream processing
- Compare exports against the source workbook
- Preserve the structure required for Google Classroom import
- Validate that no rubric criteria, levels, points, or standards links are lost during conversion

## Open questions

- Does the working workbook contain more than one worksheet?
- Are merged cells or formatting semantically important?
- Are formulas used, or is the workbook primarily a structured template?
- Does Google Classroom require a particular CSV layout for rubric import?
- Should the system generate the TSV automatically from the workbook?
- Should the repository retain both source and normalized representations?
