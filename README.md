# Cortex

`cortex/` is the operational memory, issue-tracking system, and change history for this repository.

It is organized into three areas plus one workflow file:

- `cortex/docs/`: stable project knowledge
- `cortex/issues/`: active work tracking
- `cortex/changelog/`: change history
- `cortex/workflow.md`: task-handling process

Use `cortex/docs/` to answer:

- what the system is
- how it works
- how to use it

Use `cortex/issues/` to answer:

- what needs to be done
- what is being worked on
- what has been finished

Use `cortex/changelog/` to answer:

- what changed over time

## Layout

```text
cortex/
├── workflow.md
├── changelog/
│   ├── entries/
│   ├── CHANGE_INDEX.md
│   └── README.md
├── docs/
│   ├── method/
│   ├── usage/
│   └── README.md
└── issues/
    ├── active/
    ├── backlog/
    ├── closed/
    └── README.md
```

## Entry Points

- Use `cortex/workflow.md` for the task lifecycle.
- Use `cortex/issues/README.md` for issue folder meanings.
- Use `cortex/issues/format.md` for the issue format and field rules.
- Use `cortex/changelog/README.md` for changelog folder meaning.
- Use `cortex/changelog/format.md` for the changelog format and index rules.

## Operating Rules

- Put durable knowledge in `cortex/docs/`.
- Put execution state in `cortex/issues/`.
- Put change history in `cortex/changelog/`.
- Follow `cortex/workflow.md` for task handling and lifecycle rules.
- Follow `cortex/issues/format.md` for issue format rules.
- Follow `cortex/changelog/format.md` for changelog format rules.
