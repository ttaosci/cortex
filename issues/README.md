# Issue Tracking

`issues/` is the execution system inside Cortex.

It tracks planned work, active work, and completed work.

## Structure

- `active/`: tasks currently being worked on
- `backlog/`: tasks planned for later
- `closed/`: finished tasks

## State Rules

- A task starts in `backlog/` unless work begins immediately.
- Move it to `active/` when implementation starts.
- Move it to `closed/` when acceptance criteria are met.
- If a task is blocked, keep the file in `active/` and set `Status: blocked`.
- Update status in the file before moving directories.
- Keep filenames stable when moving between states so history is easy to follow.

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
- Created:
- Start Date:
- End Date:
- Last Updated:

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
- Related Docs:
- Related Changes:
```

## Field Explanations

### `# [ISSUE-ID] Title`

Short, specific name of the task. It should identify the work without needing extra context.

`ISSUE-ID` must use a zero-padded 5-digit format: `ISSUE-00001`, `ISSUE-00042`, `ISSUE-01357`.

### `## Dates`

Lifecycle timestamps for the issue.

- `Created`: when the issue file was first created.
- `Start Date`: when actual work on the issue began.
- `End Date`: when the issue was completed and closed.
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

### `## Notes`

Optional assumptions, risks, links, references, or extra implementation details that do not belong in the main sections.

### `## Related`

Pointers to connected work and documentation.

- `Related Issues`: other issue files that are connected to this work.
- `Related Docs`: relevant documentation files in `docs/` or elsewhere.
- `Related Changes`: related code changes, changelog entries, commits, or PR references.
