# Dev Bible: AI-Assisted Delivery System

This repository is a starter workflow for shipping software with Cursor, GitHub Issues, and GitHub Projects.

## System goals

- Convert ideas into scoped plans quickly.
- Break plans into clear, testable issues.
- Execute one issue at a time with tight scope.
- Keep progress visible through a GitHub kanban board.
- Maintain quality through structured review and QA evidence.

## Repository map

- `.cursor/rules/` - persistent working rules for quality, safety, testing, and context.
- `.cursor/skills/` - reusable workflows for planning, issue generation, implementation, review, and kanban ops.
- `.cursor/plans/` - scratchpad plan templates for active work.
- `docs/prds/` - product requirement documents.
- `docs/issues/` - issue drafts and implementation notes.
- `docs/qa/` - test evidence and QA runbooks.

## Delivery lifecycle

1. **Plan feature**
   - Use `feature-planning` skill.
   - Produce scoped plan with measurable acceptance criteria.

2. **Write PRD**
   - Store in `docs/prds/`.
   - Include problem, goals, non-goals, constraints, and metrics.

3. **Create GitHub issues**
   - Use `prd-to-issues` skill.
   - Create one epic + child tasks with dependencies and labels.

4. **Track in GitHub Project**
   - Use `github-kanban` skill.
   - Maintain status flow: Backlog -> Ready -> In Progress -> In Review -> Done.

5. **Implement issue**
   - Use `issue-implementation` skill.
   - Keep scope aligned to issue acceptance criteria.

6. **Review and validate**
   - Use `code-review` skill for structured findings.
   - Store QA notes in `docs/qa/` and link evidence in PR.

## GitHub labels (starter set)

- Type: `feature`, `bug`, `chore`, `refactor`, `docs`
- Priority: `p0`, `p1`, `p2`, `p3`
- State: `blocked`, `needs-review`, `needs-qa`
- Domain: add repo-specific labels as needed

## Issue template standard

Every issue should include:

- Context and desired outcome
- In-scope and out-of-scope notes
- Acceptance criteria checklist
- Test plan checklist
- Links to PRD, dependencies, and project item

## Pull request standard

Every PR should include:

- Linked issue and PRD reference
- What changed and why
- Test evidence (automated and manual)
- Risk/rollback notes

## Team operating cadence

- **Daily:** triage, unblock, and update board status.
- **Weekly:** refine backlog and re-prioritize top work.
- **Per PR:** require review + tests before merge.

## Definition of done

- All acceptance criteria checked.
- Tests pass and QA evidence is attached.
- Docs and status are updated.
- PR merged and issue moved to Done.

# GitHub Board Maintenance

## Purpose

The GitHub Project board is the operating system for the project.

It must reflect reality, not just what the status field says.

AI must review the full board, comments, timelines, pull requests, and linked issues before deciding what comes next.

## Board Review Rule

Always review the entire board:

- Backlog
- Ready
- In Progress
- Review
- QA
- Blocked
- Done

Do not only review Ready and In Progress.

## Board Truth Rule

The true state of an issue is determined by:

1. Issue description
2. Acceptance criteria
3. Labels
4. Comments
5. Timeline/history
6. Linked issues
7. Linked pull requests
8. Board status

Status alone is never enough.

## Maintenance Actions

The board maintenance skill can recommend or apply:

- Move items to Blocked
- Move items to Done
- Move items to Ready
- Move items to Review or QA
- Promote backlog items
- Close duplicates
- Create follow-up issues
- Link parent/child issues
- Add blocker/follow-up labels
- Identify stale work

## Standard Prompt

Use this prompt in Cursor:

Use the github-board-maintenance skill.

Review the entire GitHub Project board.

Check:
- Backlog
- Ready
- In Progress
- Review
- QA
- Blocked
- Done

Read comments, timeline/history, linked PRs, and linked issues.

Update the board if needed.

Then tell me the single true next priority item.

## Quick Priority Prompt

Use this when you only want the next item:

Use the github-board-maintenance skill.

Review the entire board, not just Ready and In Progress.
Check comments, history, linked PRs, and linked issues.

Return the single highest-priority actionable issue.

## Sub-Issue Rule

If implementation reveals new required work:

- Create a follow-up issue
- Link it to the parent
- Decide whether the parent is blocked
- Update board status accordingly

## Board Hygiene Checklist

Before starting work:

- Are blocked items actually marked Blocked?
- Are completed items marked Done?
- Are Review/QA items stale?
- Are follow-up issues linked?
- Are duplicates closed or merged?
- Are Ready items truly ready?
- Are backlog items still valid?
