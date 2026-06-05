# Automation Run Lifecycle

## Purpose
Coordinate a temporary automation run from owner activation through closeout.

## Lifecycle
1. Owner activates automation with explicit scope.
2. Codex confirms the current boundary.
3. Codex performs only routine safe work inside the boundary.
4. Codex hard-stops on prohibited categories.
5. Codex verifies using the declared route.
6. Codex creates a local commit only if verification passes and commit is explicitly allowed.
7. Codex produces the full automation report.
8. Owner decides whether to continue, close, push, or escalate.

## Routing
- Activation: `skills/scoped-automation-activation.md`
- Boundary check: `practices/boundary-before-execution.md`
- Hard stops: `skills/hard-stop-boundary-enforcement.md`
- Local commit: `skills/local-milestone-commit.md`
- Closeout: `skills/automation-closeout-report.md`
- Optional email: `skills/session-report-emailing.md`

## Stop Conditions
- Scope is unclear.
- Changed files would exceed allowed files or domains.
- Verification route is missing.
- Commit or push permission is ambiguous.
- A hard-stop category appears necessary.
- Secrets or external services enter scope.
