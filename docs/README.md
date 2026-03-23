# Cortex Docs

`cortex/docs/` is the project knowledge area inside Cortex.

It stores durable knowledge that should remain useful after a task is closed.

## Structure

- `cortex/docs/method/`: pipeline design, architecture, and step-by-step system behavior
- `cortex/docs/usage/`: setup, commands, workflows, and operational guidance

## Method And Usage Rules

- Prefer stable explanations over task-specific notes.
- Keep one topic per file when possible.
- Use explicit filenames such as `quickstart.md`.
- Link related issue files when a doc was added or updated because of a task.

## Recommended Flow

1. Add or update a focused file under `cortex/docs/method/` or `cortex/docs/usage/`.
2. Reference the doc update from the corresponding issue.
