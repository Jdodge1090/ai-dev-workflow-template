# Testing Rule

Purpose: enforce reliable verification for every behavior change.

## Testing policy

- Every user-visible behavior change must include verification.
- Favor fast, deterministic tests near the changed code.
- Add regression tests for bug fixes when practical.
- Avoid brittle snapshot-only coverage without assertions on behavior.

## Required evidence in PR

- Unit/integration test updates for logic changes.
- Manual QA steps when automation is missing.
- Clear expected vs actual outcomes.
- Notes on edge cases and non-happy paths.

## Test selection guidance

- Unit tests for pure logic and transformations.
- Integration tests for service boundaries.
- End-to-end tests for critical user workflows.
- Contract tests where external APIs are involved.
