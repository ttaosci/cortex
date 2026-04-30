# Issue Format

Follow this file for the canonical issue format and field rules.

## Issue Naming

- Issue file names must use the format `ISSUE-00001_short_title.md`.
- Use a short, lowercase, underscore-separated title in the file name.
- The in-file title must use the format `# [ISSUE-00001] Title`.
- The issue ID in the file name and the in-file title must match exactly.

## Issue Format

Use this structure for standard issue files:

```md
# [ISSUE-00001] Title

## Dates
- Created: 2026-03-23T14:05:12-04:00
- Start: 2026-03-23T14:05:12-04:00
- End: 2026-03-23T14:05:12-04:00
- Last Updated: 2026-03-23T14:05:12-04:00

## Original User Prompt
> Paste the original user request here.

## Task
Short technical restatement of the task.

## Type
feature

## Status
backlog

## Priority
medium

## Background
Context, motivation, and why this task exists.

## Scope
- ...
- ...

## Acceptance Criteria
- [ ] clear outcome 1
- [ ] clear outcome 2

## Notes
Optional assumptions, risks, references, or implementation details.

## Related
- Related Issues:
- Related References:
```

## Default Values

- `Type`: `feature`
- `Status`: `backlog`
- `Priority`: `medium`
- `Acceptance Criteria`: author sign-off by default, unless the issue explicitly defines a different rule

## Field Explanations

### `# [ISSUE-ID] Title`

Short, specific name of the task. It should identify the work without needing extra context.

`ISSUE-ID` must use a zero-padded 5-digit format, and each new issue must use the next available ID in sequence, for example `ISSUE-00001`, `ISSUE-00002`, `ISSUE-00003`.

### `## Dates`

Lifecycle timestamps for the issue.

- Use ISO 8601 with timezone offset for all date fields, for example `2026-03-23T14:05:12-04:00`.
- The timezone offset should match the actual local timezone at the time of the update.
- `Created`: when the issue file was first created.
- `Start`: when actual work on the issue began.
- `End`: when the issue was completed and closed.
- `Last Updated`: when the issue file was last meaningfully updated.

### `## Original User Prompt`

The original user request or instruction that led to this issue. Keep it verbatim when possible.

### `## Task`

A short technical restatement of the work to be done. This should be clearer and more actionable than the raw prompt.

### `## Type`

The kind of work this issue represents.

Allowed values: `bug` | `feature` | `research` | `refactor` | `docs` | `tech debt`

### `## Status`

The current state of the issue.

Allowed values: `backlog` | `active` | `blocked` | `closed`

### `## Priority`

Relative urgency of the issue compared with other work.

Allowed values: `high` | `medium` | `low`

### `## Background`

Important context, motivation, or reasoning behind the issue.

### `## Scope`

The work that this issue is intended to cover. List concrete in-scope items. Do not modify files or areas that are not mentioned here unless the scope is explicitly updated.

### `## Acceptance Criteria`

The conditions that must be true for the issue to be considered done.

By default, acceptance criteria include author sign-off.
If the default sign-off rule is intended, it does not need to be repeated explicitly in every issue.
If an issue needs a different acceptance rule, write that explicitly in `Acceptance Criteria`.
Sign-off, when required, is one of the acceptance criteria.

### `## Notes`

Optional assumptions, risks, links, references, or extra implementation details that do not belong in the main sections.

### `## Related`

Pointers to connected work.

- `Related Issues`: other issue files that are connected to this work.
- `Related References`: relevant docs, prior changes, changelog entries, code paths, commits, PRs, or other references that help explain the issue context. These do not need to be files changed by the issue itself.
