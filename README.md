# Cortex

`cortex/` is the operational memory and issue-tracking system for this repository.

It is split into two parts:

- `docs/`: stable project knowledge
- `issues/`: active work tracking

Use `docs/` to answer:

- what the system is
- how it works
- how to use it
- what changed

Use `issues/` to answer:

- what needs to be done
- what is being worked on
- what has been finished

## Layout

```text
cortex/
├── docs/
│   ├── method/
│   ├── usage/
│   ├── changelog/
│   └── README.md
└── issues/
    ├── active/
    ├── backlog/
    ├── closed/
    └── README.md
```

## Operating Rules

- Put durable knowledge in `docs/`, not in issue files.
- Put execution state in `issues/`, not in docs.
- When work changes behavior, update both the relevant doc and the related issue.
- When work finishes, move the issue from `active/` to `closed/`.
- When a new task is identified but not started, create it in `backlog/`.
