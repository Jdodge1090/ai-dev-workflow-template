---
name: issue-implementation
description: Execute a single GitHub issue with disciplined scope control, implementation notes, tests, and PR-ready outputs. Use when coding work is tied to an issue and needs a reliable delivery workflow.
---

# Issue Implementation

## Objective

Deliver one issue end-to-end with clear traceability and verification.

## Workflow

1. Restate issue objective and non-goals.
2. Confirm acceptance criteria before editing code.
3. Implement in small commits or coherent edit batches.
4. Run targeted tests and capture results.
5. Update docs and issue notes with decisions.
6. Prepare PR summary linking issue and test evidence.

## Scope discipline

- Do not mix unrelated refactors with feature work.
- If new work appears, create follow-up issue instead of expanding scope.
- Keep behavior changes tied to acceptance criteria only.

## PR-ready checklist

- [ ] Acceptance criteria satisfied.
- [ ] Tests added/updated and passing.
- [ ] Migration/config notes documented if applicable.
- [ ] Issue comment added with progress and evidence.
