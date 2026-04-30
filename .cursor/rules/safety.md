# Safety Rule

Purpose: reduce regressions, avoid unsafe changes, and keep history recoverable.

## Guardrails

- Never perform destructive git operations unless explicitly requested.
- Do not commit secrets, credentials, or environment files with sensitive values.
- Prefer explicit error handling over silent failures.
- Validate inputs at boundaries (API, CLI, file, and config parsing).
- Keep dependencies current and minimal; remove unused packages.

## Change safety checklist

- Is the blast radius understood?
- Is backward compatibility considered?
- Are failure modes handled and observable?
- Can the change be rolled back quickly?
- Is there monitoring or logging for critical paths?

## Security minimums

- No hardcoded secrets or tokens.
- Principle of least privilege for integrations and automation.
- Escape or validate untrusted input.
- Review auth and permission checks in changed paths.
