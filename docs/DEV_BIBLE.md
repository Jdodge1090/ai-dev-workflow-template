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
