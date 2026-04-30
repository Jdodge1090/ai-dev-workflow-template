---
name: prd-to-issues
description: Translate a PRD into a structured GitHub issue set with epic/task hierarchy, labels, dependencies, and acceptance criteria. Use when a PRD exists and execution-ready issues are needed.
---

# PRD to Issues

## Objective

Turn one PRD into an actionable set of GitHub issues that can be tracked in a project board.

## Workflow

1. Parse PRD goals, constraints, and non-goals.
2. Create one epic issue for the PRD.
3. Derive child tasks sized for 0.5-2 days each when possible.
4. Add acceptance criteria to every child issue.
5. Add dependency links and execution order.
6. Recommend labels, assignee role, and project status column.

## Issue writing rules

- Title uses verb + outcome (`Implement`, `Add`, `Refactor`, `Fix`).
- Body includes: context, scope, acceptance criteria, test plan.
- Explicitly call out blocked-by or blocks relationships.
- Include PRD reference at top of each issue.

## Output template

```markdown
## Epic
- Title: ...
- Body: ...

## Child issues
1. Title: ...
   Labels: ...
   Depends on: ...
   Acceptance criteria:
   - [ ] ...
```
