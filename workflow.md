# Cortex Workflow

This document defines how a new task should be handled in Cortex.

## New Task Flow

1. Create an issue immediately from the query.
   - Follow `cortex/issues/format.md` for the issue format and field rules.

2. Record the original request exactly.
   - Put the raw query under `Original User Prompt`.
   - Add a short `Task` section that rewrites it in clear engineering language.

3. Save the issue in `cortex/issues/backlog/` first.
   - Every new task starts in backlog before execution.

4. Clarify the task before implementation.
   - scope
   - acceptance criteria
   - assumptions
   - dependencies
   - related docs, issues, or prior changes
   - If any required field is unclear, stop and ask the person or agent that made the query before proceeding.

5. Decide whether the task is ready.
   - If the task is still unclear, keep it in `cortex/issues/backlog/`.
   - If the task is blocked before execution starts, keep it in `cortex/issues/backlog/` and mark that clearly in the issue.
   - If the task becomes blocked after execution starts, keep it in `cortex/issues/active/` and set `Status: blocked`.

6. Start work only when execution is explicitly chosen.
   - Move the issue from `cortex/issues/backlog/` to `cortex/issues/active/`.
   - Set `Status: active` and fill `Start`.

7. Keep the issue updated during execution.
   - Record major decisions, scope changes, blockers, and important findings in the issue.
   - Follow `cortex/issues/format.md` whenever creating or modifying an issue.
   - Update `Last Updated` when the issue changes meaningfully.
   - Note: do not modify `ISSUE-ID`, `Created`, `Start`, or `Original User Prompt` after the issue is created, except to fill `Start` once when work actually begins.

8. When the task is complete:
   - Follow `cortex/changelog/format.md` to create a changelog entry under `cortex/changelog/entries/` and update `cortex/changelog/CHANGE_INDEX.md`.
   - Make sure the `Related` section reflects the final state of the issue.
   - Obtain required sign-off according to the issue's acceptance criteria. By default, this means author sign-off unless the issue explicitly defines a different rule. Any required sign-off must cover the full final state of the issue, including the changelog entry and the `Related` section.
   - Verify that all acceptance criteria are met.
   - Set `Status: closed`, fill in `End`, and update `Last Updated`.
   - Move the issue to `cortex/issues/closed/`.
