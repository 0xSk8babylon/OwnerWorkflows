# First Push

## Purpose
Publish a new repository branch for the first time.

## When To Use
Use after a local repo has commits, a clean status, and a configured remote.

## Procedure / Checklist
- Confirm `pwd`.
- Run `git status --short`.
- Run `git branch --show-current`.
- Run `git remote -v`.
- Run `git log --oneline -5`.
- Confirm branch, remote, and commits.
- Treat "safe to push" as readiness for owner review, not permission to push.
- Ask owner approval before pushing.
- Push normally and verify status.

## Commands
- `git push -u origin <branch>`
- `git status --short`

## Stop Conditions
- Working tree is dirty.
- Branch is not the intended default.
- Remote is missing or incorrect.
- Authentication is unavailable.

## Owner Approval Gates
- Required before first push.
- Separate from commit approval.

## Constraints
- Do not force push.
- Do not rewrite history.
- Do not publish before approval.
