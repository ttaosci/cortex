# Cortex Workflow

This document defines how a new task should be handled in Cortex.

## New Task Flow

1. Create an issue immediately from the query.
   - Follow `references/issues_format.md` for the issue format and field rules.

2. Record the original request exactly.
   - Put the raw query under `Original User Prompt`.
   - Add a short `Task` section that rewrites it in clear engineering language.
   - Search for related issues and related references, then update the current issue.

3. Save the issue in `issues/backlog/` first.
   - Every new task starts in backlog before execution.

4. Clarify the task before implementation.
   - scope
   - acceptance criteria
   - assumptions
   - dependencies
   - related docs, issues, or prior changes
   - If any required field is unclear, stop and ask the person or agent that made the query before proceeding.

5. Start work only after the user explicitly chooses to execute.
   - Move the issue from `issues/backlog/` to `issues/active/`.
   - Set `Status: active` and fill `Start`.

6. Keep the issue updated during execution.
   - Record major decisions, scope changes, blockers, and important findings in the issue.
   - Follow `references/issue_format.md` whenever creating or modifying an issue.
   - Update `Last Updated` when the issue changes meaningfully.
   - Do NOT modify `ISSUE-ID` or `Original User Prompt` after the issue is created.
   - Do NOT add changelog in this stage.

7. When the task is complete:
   - Follow `references/changelog_format.md` to create a changelog entry under `changelog/entries/` and update `changelog/CHANGE_INDEX.md`.
   - Make sure the `Related` section reflects the final state of the issue.
   - Obtain required sign-off according to the issue's acceptance criteria. By default, this means author sign-off unless the issue explicitly defines a different rule. Any required sign-off must cover the full final state of the issue, including the changelog entry and the `Related` section.
   - Verify that all acceptance criteria are met.
   - Set `Status: closed`, fill in `End`, and update `Last Updated`.
   - Move the issue to `issues/closed/`.
