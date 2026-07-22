# Intake — Class Template Zips (and future material)

**Produced by: Claude Fable 5.** Status: v1.0, 2026-07-22.

## Where Geoff drops files (watched locations, verified on this machine)

**Primary — Google Drive transfer folder** (the Drive↔Mac-mini document
channel; local sync path):

```
/Users/lcars/Library/CloudStorage/GoogleDrive-professionalcustomer@gmail.com/My Drive/Transfer - Shared/
```

**Secondary — local pipeline transfer folder** (also acceptable):

```
/Users/lcars/Projects/Transfer/
```

(Other Drive folders JTransfer / "Photo Transfer " are photo channels —
not used for class-align intake.)

## Expected drop: two zips

Most-recent-incarnation Google Classroom templates for the two priority
classes (10th CP, 11th CP). Names may vary; identify by content, not name.

## Intake procedure (WP C1.1 executes this)

1. Detect zip(s) in a watched folder; copy (never move — Geoff cleans his
   own transfer folder) to `/tmp/class-align-intake/`.
2. `unzip -l` FIRST: inventory + confirm class identity from contents;
   record zip sha256.
3. **Privacy gate before anything lands in the repo:** scan the listing
   and sampled contents for student-identifying material (C0.3 checker
   when built; manual three-state check until then). Files with student
   data → `protected/<class>/` (gitignored), NEVER `sources/`.
4. Clean teacher-authored material → `sources/classes/<10cp|11cp>/`
   preserving the zip's internal folder structure (planning doc: structure
   is signal for assignment grouping).
5. Write `sources/classes/<class>/INTAKE_RECORD.md`: zip name, sha256,
   date, file count, structure summary, privacy-gate outcome, anything
   quarantined to protected/.
6. Commit ("Intake: <class> templates <date>"), push, update
   PROJECT_STATE.md (unblocks C1.2).

## Landing map

| Content | Lands in |
|---------|----------|
| Teacher templates, directions, slides, rubrics | `sources/classes/<class>/…` |
| Anything with student names/work | `protected/<class>/…` (gitignored) |
| Original zips | NOT stored in repo; sha256 in INTAKE_RECORD.md (Drive keeps the original) |

## Standing rule

Any future material follows the same path: watched folder → inventory →
privacy gate → sources/ or protected/ → INTAKE_RECORD → commit.
