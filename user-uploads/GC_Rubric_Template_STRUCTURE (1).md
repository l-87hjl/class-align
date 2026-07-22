# GC Rubric Template Structure

*Plain-text companion guide for `GC_Rubric_Template_WORKING.xlsx`*

This file explains the Google Classroom rubric spreadsheet structure in a format that is easy for an AI or human to read. The `.xlsx` file remains the actual working template for Google Classroom import. This `.md` file is only a structure guide.

---

## Purpose

Use this file with the authoritative rubric directions and the working Excel template.

- `GC_Rubric_Directions_CURRENT_v01.06.md` explains the rubric method and grading philosophy.
- `GC_Rubric_Template_WORKING.xlsx` provides the actual Google Classroom import format.
- `GC_Rubric_Template_STRUCTURE.md` explains the row/block layout in plain text.

When creating a Google Classroom rubric, preserve the Excel structure from the working `.xlsx` template and replace only the rubric content.

---

## Required Google Classroom Header Rows

The spreadsheet must begin with these rows exactly:

```text
Row 1: It is recommended that you do not edit rubrics in spreadsheet format.
Row 2: v1.0-s
```

Do not add a normal table header such as `Criteria / Description / Level 4 / Level 3`.

---

## Criterion Block Pattern

Each rubric criterion uses a **5-row block**.

```text
Criterion Block Row 1: Criterion title
Criterion Block Row 2: Criterion description
Criterion Block Row 3: Level point values across columns B-F
Criterion Block Row 4: Level names across columns B-F
Criterion Block Row 5: Level descriptions across columns B-F
```

Columns B-F usually represent the five levels:

```text
Column B: Level 4 - Advanced
Column C: Level 3 - Proficient
Column D: Level 2 - Progressing
Column E: Level 1 - Developing
Column F: Level 0 - Missing / Not Assessable
```

---

## Standards-Based Criterion Pattern

Each selected CA CCSS standard should usually become its own 0-4 criterion.

The criterion title should begin with the standard code so the teacher can easily match it to the tagged Google Classroom learning goal.

Example:

```text
RL.9-10.2 - Theme / Central Idea Development
```

Standard criterion point values should usually be:

```text
4 | 3 | 2 | 1 | 0
```

Standard criterion level names should usually be:

```text
Advanced | Proficient | Progressing | Developing | Missing / Not Assessable
```

Remember:

```text
3 = Proficient / meets the standard
4 = Advanced / exceeds the standard
```

Do not treat 4 as the only successful score.

---

## Holistic Criterion Pattern

After all selected standards have their own 0-4 criteria, put all remaining points into one large holistic category.

Recommended title:

```text
Holistic Assignment Performance - Completion, Effort, Organization, and Overall Quality
```

The holistic category usually stays unlinked to a CA CCSS standard because it is for completion, effort, following directions, overall quality, coherence, and grading flexibility.

Holistic points formula:

```text
Holistic points = Total assignment points - (number of standards x 4)
```

Holistic level point spread:

```text
Advanced = 100% of holistic points
Proficient = 85% of holistic points
Progressing = 75% of holistic points
Developing = 63% of holistic points
Missing / Not Assessable = 0% of holistic points
```

Round only when needed for Google Classroom import.

---

## Example: 20-Point Rubric with 4 Standards

```text
4 standards x 4 points = 16 standards points
20 total points - 16 standards points = 4 holistic points
```

| Criterion | Advanced | Proficient | Progressing | Developing | Missing |
|---|---:|---:|---:|---:|---:|
| Standard 1 | 4 | 3 | 2 | 1 | 0 |
| Standard 2 | 4 | 3 | 2 | 1 | 0 |
| Standard 3 | 4 | 3 | 2 | 1 | 0 |
| Standard 4 | 4 | 3 | 2 | 1 | 0 |
| Holistic Assignment Performance | 4 | 3.4 | 3 | 2.52 | 0 |

For Google Classroom, holistic values may be rounded if necessary while preserving the 100 / 85 / 75 / 63 / 0 pattern.

---

## Example: 200-Point Rubric with 6 Standards

```text
6 standards x 4 points = 24 standards points
200 total points - 24 standards points = 176 holistic points
```

| Criterion | Advanced | Proficient | Progressing | Developing | Missing |
|---|---:|---:|---:|---:|---:|
| Standard 1 | 4 | 3 | 2 | 1 | 0 |
| Standard 2 | 4 | 3 | 2 | 1 | 0 |
| Standard 3 | 4 | 3 | 2 | 1 | 0 |
| Standard 4 | 4 | 3 | 2 | 1 | 0 |
| Standard 5 | 4 | 3 | 2 | 1 | 0 |
| Standard 6 | 4 | 3 | 2 | 1 | 0 |
| Holistic Assignment Performance | 176 | 149.6 | 132 | 110.88 | 0 |

---

## Category Limit

Google Classroom allows a maximum of 10 rubric criteria/categories in an imported rubric.

Because this rubric system reserves one category for holistic assignment performance, the practical maximum is:

```text
9 standards-based categories + 1 holistic category = 10 categories total
```

If more than 9 standards seem relevant, choose the 9 strongest standards and absorb the rest into the closest matching standard category or holistic category.

---

## Content Replacement Rules

When generating a new rubric from the Excel template:

1. Preserve the Google Classroom spreadsheet layout exactly.
2. Replace placeholder standard titles with real CA CCSS-aligned criterion titles.
3. Replace placeholder descriptions with assignment-specific descriptions.
4. Keep standards categories as 0-4 criteria unless there is a clear reason not to.
5. Recalculate holistic points based on the requested total assignment value.
6. Keep one holistic category for remaining completion / effort / organization / overall quality points.
7. Do not add extra rows, notes, headers, merged cells, or explanatory sections inside the spreadsheet.

---

## One-Sentence Structure Rule

Start from the working Google Classroom Excel template, preserve the required header rows and 5-row criterion block format, create one 0-4 category for each selected CA CCSS standard, then place all remaining assignment points into one holistic performance category using the 100 / 85 / 75 / 63 / 0 point spread.
