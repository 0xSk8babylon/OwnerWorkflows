# Owner-Controlled Escalation

## Purpose
Separate routine safe automation from high-risk owner decisions.

## Practice
- Routine safe work can be automated inside a declared scope.
- High-risk work cannot be automated.
- Unclear scope stops the run.
- The owner decides manually in a separate session.
- Codex must not negotiate dangerous escalation in the middle of an automation run.

## High-Risk Work
- Git push.
- Migrations.
- Auth, security, or permission enforcement.
- Deleting files.
- Doctrine rewrites.
- Scope changes.
- External services or secrets.
- Broad refactors.
- Billing.
- Production deployment.
- Destructive commands.

## Report Expectations
- State the escalation trigger.
- State why the run stopped.
- State what remains safe to do.
- State what owner decision is required separately.

## Cross-References
- `practices/milestone-approval-gates.md`
- `practices/non-destructive-git.md`
- `skills/hard-stop-boundary-enforcement.md`
