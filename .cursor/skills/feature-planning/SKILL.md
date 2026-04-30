---
name: feature-planning
description: Convert a feature request into an implementation-ready plan with scope, risks, milestones, and acceptance criteria. Use when the user asks to plan a feature, break down work, or clarify delivery approach.
---

# Feature Planning

## Objective

Produce a concise implementation plan that is ready to become a PRD and GitHub issues.

## Workflow

1. Clarify problem, users, and expected outcome.
2. Define in-scope and out-of-scope boundaries.
3. Write acceptance criteria that are testable.
4. Identify risks, dependencies, and rollout constraints.
5. Split the work into milestones and deliverables.
6. Propose initial issue breakdown and labels.

## Output template

Use this structure:

```markdown
# Feature Plan: <name>

## Problem
<what is broken or missing>

## Outcome
<target behavior and user value>

## Scope
- In: ...
- Out: ...

## Acceptance criteria
- [ ] ...
- [ ] ...

## Risks and dependencies
- Risk: ... | Mitigation: ...

## Milestones
1. ...
2. ...

## Issue seed list
- Epic: ...
- Task: ...
```

## Quality bar

- Keep assumptions explicit.
- Keep criteria measurable.
- Default to small, reviewable increments.
