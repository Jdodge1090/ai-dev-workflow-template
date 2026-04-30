# Project Rule

Purpose: keep implementation aligned with product intent and repository standards.

## Core directives

- Treat `docs/DEV_BIBLE.md` as the operating contract for this repository.
- Prefer incremental, reviewable changes over large rewrites.
- Keep docs and issue artifacts updated as part of each feature or fix.
- Reference an issue in every substantive implementation task.
- Preserve existing behavior unless the issue explicitly calls for a change.

## Definition of ready (before coding)

- Problem statement is clear and scoped.
- Acceptance criteria are testable.
- Dependencies and risks are identified.
- Work is mapped to one issue with labels and project status.

## Definition of done (before merge)

- Acceptance criteria are met.
- Tests are added or updated for changed behavior.
- Docs are updated (`docs/prds`, `docs/issues`, `docs/qa` as needed).
- PR links to issue, includes test evidence, and passes CI.
