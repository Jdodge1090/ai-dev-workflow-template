# GitHub Board Maintenance Skill

Purpose:
Maintain the entire GitHub Project board so it reflects the real state of work.

This skill reviews all board items, issue comments, timelines, linked issues, pull requests, blockers, follow-ups, and completion signals.

It is used to:
- Find the true next priority
- Update blocked work
- Move completed work to Done
- Move ready work forward
- Review backlog quality
- Detect stale items
- Identify missing follow-up issues
- Keep parent/child issue relationships accurate

---

## Required Scope

When running this skill, review the entire board, including:

- Backlog
- Ready
- In Progress
- Review
- QA
- Blocked
- Done

Do not only review Ready and In Progress.

---

## Required Process

1. Load all board items.
2. For each issue/item, review:
   - Title
   - Description
   - Labels
   - Priority
   - Status
   - Assignee
   - Linked pull requests
   - Issue comments
   - Timeline/history
   - Linked issues
   - References to blockers or follow-ups

3. Determine actual state:
   - Is it actionable?
   - Is it blocked?
   - Is it stale?
   - Is it duplicated?
   - Is it superseded?
   - Is it completed?
   - Is it missing acceptance criteria?
   - Did it create follow-up/sub-issues?
   - Does another issue need to happen first?

4. Recommend and, when explicitly asked, apply updates:
   - Move blocked items to Blocked
   - Move completed items to Done
   - Move reviewed items to QA or Done
   - Move actionable items to Ready
   - Move active work to In Progress
   - Reprioritize based on blockers/follow-ups
   - Add labels such as blocked, follow-up, needs-review, stale, duplicate
   - Link parent/child issues where appropriate
   - Create follow-up issues when discovered

---

## Status Rules

### Backlog
Use when:
- Work is valid but not ready
- Requirements are incomplete
- Lower priority
- Future enhancement

### Ready
Use when:
- Requirements are clear
- Acceptance criteria exist
- No blockers exist
- Work can begin now

### In Progress
Use when:
- Someone is actively working on it
- It is not blocked
- It has not been superseded

### Review
Use when:
- Code has been implemented
- A PR/diff exists
- Human or AI review is needed

### QA
Use when:
- Review is complete
- Manual verification is needed
- Feature needs real-world testing

### Blocked
Use when:
- Another issue must be completed first
- A bug prevents completion
- Requirements are unresolved
- Comments/history show it cannot proceed

### Done
Use when:
- Acceptance criteria are met
- PR is merged or implementation is complete
- No unresolved blockers remain
- Follow-up issues have been created for remaining work

---

## Priority Rules

Determine priority from the whole board using this order:

1. Active blockers preventing other work
2. P0 issues that are actionable
3. Follow-up issues required to complete active work
4. In Progress work that is still valid and unblocked
5. Ready work with clear acceptance criteria
6. Review/QA items close to completion
7. Backlog items that should be promoted
8. Everything else

Never trust the board status alone.

Comments and timeline/history may override status.

Newer linked issues may supersede older ones.

---

## Required Outputs

When asked to maintain the board, return:

# GitHub Board Maintenance Report

## Updates Needed

List each recommended board update:

- Issue:
- Current Status:
- Recommended Status:
- Reason:
- Required Action:

## Blockers Found

List blocked items and what blocks them.

## Items Ready to Work

List actionable Ready items.

## Items That Should Move to Done

List completed items.

## Backlog Review

List backlog items that should be promoted, clarified, merged, or closed.

## Follow-Up/Sub-Issues Needed

List new issues that should be created.

## True Next Priority

Return one single issue:

#<issue_number> — <title>

Reason: <short reason>

---

## Output Rule for Quick Priority Request

If the user asks only for the next priority item, still review the full board first.

Then return only:

#<issue_number> — <title>
Reason: <one-line reason>

---

## Update Permission Rule

Do not modify the GitHub board unless the user explicitly asks to update it.

If asked to update the board:
- Apply status changes
- Apply labels
- Link related issues
- Create follow-up issues if needed
- Summarize all changes made

---

## Implementation Rule

When implementing any issue:

If new work is discovered:
- Do not silently expand scope
- Create or recommend a follow-up issue
- Link it to the parent issue
- Mark the parent blocked if the follow-up must happen first
