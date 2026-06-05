# Boundary Before Execution

## Purpose
Confirm the operating boundary before any automated run changes files.

## Required Boundary
Identify:

- Current repo.
- Current branch.
- Current scope.
- Current continuity docs.
- Current dirty state.
- Next safe boundary.
- Prohibited actions.
- Verification route.
- Commit permission.
- Push permission.

## Procedure
- Run `git status --short`.
- Run `git branch --show-current`.
- Inspect the smallest relevant navigation, index, or continuity docs.
- State the planned route before edits.
- Stop if scope, verification, commit permission, or push permission is unclear.

## Cross-References
- `practices/repo-state-inspection.md`
- `practices/context-routing.md`
- `practices/negative-constraints.md`
- `practices/milestone-approval-gates.md`
