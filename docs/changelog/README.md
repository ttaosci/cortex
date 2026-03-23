# Changelog

Use this directory to record meaningful repository and workflow changes over time.

## Purpose

Each changelog entry should make it easy to answer:

- what changed
- which issue the change belongs to
- which related files were touched

## Entry Format

Each entry should use this structure:

```md
## YYYY-MM-DD - Title
Issue: ISSUE-00001
Related Files:
- path/to/file.md
- path/to/code.py
Summary:
- ...
```

## Fields

- `Issue`: corresponding issue ID, matching the real issue ID in zero-padded 5-digit format
- `Related Files`: docs, code, or other files related to the change
- `Summary`: short factual bullets describing the change

## Rules

- Prefer one entry per meaningful shipped change or workflow change.
- Keep entries in reverse chronological order.
- Keep `Summary` factual and concrete.
- Always include an issue reference, even for docs-only changes.
- Always include `Related Files`. If there are no related files to list, write `None`.
- Use zero-padded 5-digit issue IDs, for example `ISSUE-00001`.
- Make `Summary` as concise as possible while still being complete and easy to understand.

## Change Index Format

`CHANGE_INDEX.md` is a compact index of changelog entries, not a place for full entry content.

Recommended structure:

```md
# Change Index

## 2026
- 2026-03-22 | ISSUE-00001 | Establish Cortex | 2026-03-22-ISSUE-00001-establish-cortex.md
- 2026-03-21 | ISSUE-00002 | Update CLI quickstart | 2026-03-21-ISSUE-00002-update-cli-quickstart.md
```

Each index line should contain:

- `Date`
- `Issue`
- `Title`
- `Entry File`

Index rules:

- Group entries by year.
- Keep entries in reverse chronological order within each year.
- Use one line per changelog entry.
- Do not duplicate full summaries in `CHANGE_INDEX.md`.
- Use filenames in the format `YYYY-MM-DD-ISSUE-00001-short-title.md`.

## Example

```md
## 2026-03-22 - Establish Cortex
Issue: ISSUE-00001
Related Files:
- README.md
- docs/README.md
- issues/README.md
Summary:
- Established Cortex as the documentation and issue-tracking system.
- Defined `docs/` as durable project knowledge.
- Defined `issues/` as execution tracking.
- Added starter templates and README files.
```
