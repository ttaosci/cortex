# Changelog Format

Follow this file for the canonical changelog format and index rules.

## Entry Format

Each entry should use this structure:

```md
## YYYY-MM-DD - Title
Issue: <ISSUE-ID>
Related Files:
- path/to/file.md
- path/to/code.py
Summary:
- ...
```

## Fields

- `Issue`: corresponding issue ID. Follow `cortex/issues/format.md` for the canonical issue format.
- `Related Files`: docs, code, or other files related to the change
- `Summary`: short factual bullets describing the change

## Rules

- Prefer one entry per meaningful shipped change or workflow change.
- Keep entries in reverse chronological order.
- Keep `Summary` factual and concrete.
- Always include an issue reference, even for docs-only changes.
- Always include `Related Files`. If there are no related files to list, write `None`.
- Entry file names must use the format `<ISSUE-ID>-short-title.md`.
- Make `Summary` as concise as possible while still being complete and easy to understand.

## Change Index Format

`cortex/changelog/CHANGE_INDEX.md` is a compact index of changelog entries, not a place for full entry content.
Full changelog entries should be stored under `cortex/changelog/entries/`.

Recommended structure:

```md
# Change Index

## 2026
- 2026-03-22 | <ISSUE-ID> | Title | entries/<ISSUE-ID>-short-title.md
- 2026-03-21 | <ISSUE-ID> | Title | entries/<ISSUE-ID>-short-title.md
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
- Do not duplicate full summaries in `cortex/changelog/CHANGE_INDEX.md`.
- Store entry files under `cortex/changelog/entries/`.
- Use filenames in the format `<ISSUE-ID>-short-title.md`.
- The `Entry File` field should use the path relative to `cortex/changelog/`, for example `entries/<ISSUE-ID>-short-title.md`.

## Example

```md
## YYYY-MM-DD - Title
Issue: <ISSUE-ID>
Related Files:
- cortex/README.md
- cortex/docs/README.md
- cortex/issues/format.md
Summary:
- Added ...
- Updated ...
```
