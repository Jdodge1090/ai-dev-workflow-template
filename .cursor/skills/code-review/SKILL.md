---
name: code-review
description: Review changes for correctness, regressions, maintainability, security, and test coverage with severity-ranked findings. Use when reviewing pull requests or validating implementation quality before merge.
---

# Code Review

## Objective

Provide actionable review feedback that improves reliability and merge confidence.

## Review order

1. Correctness and logic regressions.
2. Security and data safety concerns.
3. Test sufficiency and missing edge cases.
4. Maintainability and readability.
5. Performance or operational risks.

## Severity levels

- `critical`: must fix before merge.
- `major`: strong recommendation before merge.
- `minor`: optional improvement.

## Output format

```markdown
## Findings
1. [critical] <title>
   - Why it matters: ...
   - Evidence: ...
   - Suggested fix: ...

## Open questions
- ...

## Residual risk
- ...
```
