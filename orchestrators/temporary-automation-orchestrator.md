# Temporary Automation Orchestrator

## Purpose
Let Codex automate routine safe work inside a currently approved task, phase, or milestone while preserving owner control.

## Default State
Inactive until the owner explicitly activates it for a bounded run.

## Activation Requirements
Every activation must declare:

- Repo.
- Branch.
- Phase or task.
- Allowed files or domains.
- Forbidden actions.
- Verification required.
- Commit allowed: yes or no.
- Push allowed: no.
- Report required: yes.

If scope is vague, stop before file changes.

## Operating Rules
- Stay inside the activated boundary.
- Prefer additive changes.
- Use `practices/boundary-before-execution.md` before edits.
- Use `skills/hard-stop-boundary-enforcement.md` for prohibited categories.
- Use `skills/secret-boundary-enforcement.md` for environment and credential boundaries.
- Use `skills/automation-closeout-report.md` for the final report.
- Use `skills/local-milestone-commit.md` only if local commit is explicitly allowed.

## Allowed Automation
- Read files.
- Inspect continuity docs.
- Run tests, lint, type checks, docs checks, or formatting checks.
- Make additive implementation or docs changes inside approved scope.
- Stage approved-scope files if commit is allowed.
- Create a clean local commit if verification passes and commit is explicitly allowed.
- Produce local report artifacts.
- Print the final report.

## Hard Stops
- Git push.
- Migrations.
- Auth, security, or permission enforcement changes.
- Deleting files.
- Doctrine rewrites.
- Scope changes.
- Unrelated repo changes.
- External service setup.
- Adding or exposing secrets.
- Broad refactors.
- Billing changes.
- Production deployment.
- Destructive commands.

## No Background Promises
Do not promise future background work, monitoring, delayed retries, or later delivery. Work ends at the reported boundary.

## Owner Decision Boundary
After the report, the owner decides whether to continue, close, commit, push, or escalate in a separate approval step.
