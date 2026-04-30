# GitHub Project Setup

Use this checklist to create a kanban board that matches the Dev Bible workflow.

## Create project

1. Create a new GitHub Project (Board/Table hybrid works well).
2. Add fields:
   - `Status` (single select)
   - `Priority` (single select)
   - `Estimate` (number or single select)
3. Add default views: `Board`, `Backlog table`, `My items`.

## Status options

- Backlog
- Ready
- In Progress
- In Review
- Done

## Automation suggestions

- New item -> `Status: Backlog`
- PR opened for linked issue -> `Status: In Review`
- PR merged -> `Status: Done`

## Operating rules

- Only move to `Ready` when acceptance criteria exist.
- Keep WIP low in `In Progress`.
- Mark blocked issues with `blocked` label and comment with blocker.
