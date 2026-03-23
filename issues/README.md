# Issue Tracking

`cortex/issues/` is the execution system inside Cortex.

It tracks planned work, active work, and completed work.

## Structure

- `cortex/issues/active/`: tasks currently being worked on, including blocked tasks that have already started
- `cortex/issues/backlog/`: tasks planned for later
- `cortex/issues/closed/`: finished tasks
- `cortex/issues/format.md`: canonical issue format and field rules

## Folder Meanings

- `cortex/issues/active/`: issues that are currently being worked on, including issues with `Status: blocked` after execution has started
- `cortex/issues/backlog/`: issues that are defined but not yet being executed
- `cortex/issues/closed/`: issues that are finished and no longer active

## Notes

- Follow `cortex/workflow.md` for the issue lifecycle and state transitions.
- Follow `cortex/issues/format.md` for the canonical issue format and field rules.
