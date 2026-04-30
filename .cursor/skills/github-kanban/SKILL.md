---
name: github-kanban
description: Operate GitHub Projects as a kanban system with clear column rules, WIP limits, automation, and status hygiene. Use when setting up or managing GitHub issue flow across backlog, in progress, review, and done.
---

# GitHub Kanban

## Objective

Keep delivery flow visible and predictable using GitHub Issues + GitHub Projects.

## Recommended columns

1. `Backlog` - prioritized, not started.
2. `Ready` - scoped and acceptance criteria complete.
3. `In Progress` - actively being implemented.
4. `In Review` - PR open and awaiting review.
5. `Done` - merged and validated.

## Column entry rules

- Move to `Ready` only when issue has clear acceptance criteria.
- Move to `In Progress` only when actively worked today.
- Move to `In Review` when PR is opened.
- Move to `Done` only after merge and verification.

## WIP guidance

- Limit `In Progress` to a small number per engineer.
- Prefer finishing before starting new work.
- Flag blocked items with a `blocked` label and comment.

## Cadence

- Daily: triage new issues and blocked items.
- Weekly: prune stale backlog and refine top priorities.
