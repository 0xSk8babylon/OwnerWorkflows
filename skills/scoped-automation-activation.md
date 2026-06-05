# Scoped Automation Activation

## Purpose
Activate temporary automation only when owner control, scope, verification, and reporting are explicit.

## Required Activation Format

```text
Activate Temporary Automation Orchestrator for:

- repo:
- branch:
- phase/task:
- allowed files/domains:
- forbidden actions:
- verification required:
- commit allowed: yes/no
- push allowed: no
- report required: yes
```

## Procedure
- Confirm the request explicitly activates temporary automation.
- Confirm current repo and branch match the activation.
- Confirm allowed files or domains are concrete.
- Confirm forbidden actions include all hard-stop categories or a stricter subset.
- Confirm verification is declared.
- Confirm push allowed is `no`.
- Confirm report required is `yes`.

## Reject Vague Requests
Stop before file changes when the activation omits or blurs:

- Repo.
- Branch.
- Phase or task.
- Allowed files or domains.
- Forbidden actions.
- Verification route.
- Commit permission.
- Push prohibition.
- Reporting requirement.

## Constraints
- Do not infer scope from prior sessions.
- Do not expand scope because the repo has related work.
- Do not turn ordinary owner approval into standing automation authority.

## Output Required
- Activated boundary.
- Verification route.
- Commit and push permissions.
- First safe action.
