# Hard Stop Boundary Enforcement

## Purpose
Teach every automation run which actions are never automated.

## Hard Stops
- Git push.
- Migrations.
- Auth, security, or permission enforcement changes.
- Deleting files.
- Doctrine rewrites.
- Scope changes.
- Unrelated repos.
- External services or secrets.
- Broad refactors.
- Billing changes.
- Production deployment.
- Destructive commands.

## Core Rule
If a hard-stop action appears necessary, stop and report. Do not ask to bypass the hard stop inside the automation run.

## Report When Stopped
- Trigger.
- Why it is outside automation authority.
- Work completed before the stop.
- Files touched.
- Verification completed or skipped.
- Owner decision needed in a separate session.

## Cross-References
- `practices/negative-constraints.md`
- `practices/non-destructive-git.md`
- `practices/milestone-approval-gates.md`
