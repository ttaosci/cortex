---
name: cortex
description: Track issues and changes in the repository. Use when the user says "cortex" or asks to create a cortex issue.
---

# Cortex

Cortex is the operational memory, issue-tracking system, and change history for this repository.

It is organized into two areas:

- `$CORTEX_HOME/issues/`: active work tracking
- `$CORTEX_HOME/changelog/`: change history

Use `$CORTEX_HOME/issues/` to answer:

- what needs to be done
- what is being worked on
- what has been finished

Use `$CORTEX_HOME/changelog/` to answer:

- what changed over time

## Layout

```text
$CORTEX_HOME
├── changelog
│   ├── CHANGE_INDEX.md
│   └── entries
└── issues
    ├── active
    ├── backlog
    └── closed
```

## Entry Points

- Use `references/workflow.md` for the task lifecycle.
- Use `references/issue.md` for issue folder meanings.
- Use `references/issue_format.md` for the issue format and field rules.
- Use `references/changelog.md` for changelog folder meaning.
- Use `references/changelog_format.md` for the changelog format and index rules.

## Operating Rules

- Put execution state in `$CORTEX_HOME/issues/`.
- Put change history in `$CORTEX_HOME/changelog/`.
- Follow `references/workflow.md` for task handling and lifecycle rules.
- Follow `references/issue_format.md` for issue format rules.
- Follow `references/changelog_format.md` for changelog format rules.
