# Cortex Docs

`docs/` is the project knowledge area inside Cortex.

It stores durable knowledge that should remain useful after a task is closed.

## Structure

- `method/`: pipeline design, architecture, and step-by-step system behavior
- `usage/`: setup, commands, workflows, and operational guidance
- `changelog/`: dated records of meaningful changes

## Writing Rules

- Prefer stable explanations over task-specific notes.
- Keep one topic per file when possible.
- Use explicit filenames such as `quickstart.md`.
- Link related issue files when a doc was added or updated because of a task.
- Update `changelog/CHANGE_INDEX.md` when behavior, structure, or workflow materially changes.

## Recommended Flow

1. Add or update a focused file under `method/` or `usage/`.
2. Record the change in `changelog/`.
3. Reference the doc update from the corresponding issue.
