# Context Rule

Purpose: keep AI-assisted work grounded in repository context and traceability.

## Context hierarchy

1. Current issue and acceptance criteria.
2. Relevant PRD in `docs/prds/`.
3. Prior implementation notes in `docs/issues/`.
4. QA evidence in `docs/qa/`.
5. Existing code and tests.

## Working norms

- Restate assumptions when requirements are ambiguous.
- Prefer reading existing patterns before introducing new ones.
- Capture key decisions in issue or PR comments to preserve context.
- If blocked, document blocker and next action in the issue.

## Traceability requirements

- Each implementation PR must link to one primary issue.
- Each issue should link back to PRD source and QA notes.
- Keep status current in GitHub Project board columns.
