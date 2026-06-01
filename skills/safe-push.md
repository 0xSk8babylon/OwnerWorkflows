# Safe Push

## Purpose
Push only owner-approved commits from a verified repo state.

## When To Use
Use before publishing an existing branch.

## Procedure / Checklist
- Confirm `pwd`.
- Run `git status --short`.
- Run `git branch --show-current`.
- Run `git remote -v`.
- Run `git log --oneline -5`.
- Confirm branch, remote, status, and commits with owner.
- Push only after approval.

## Commands
- `git push origin <branch>`
- `git status --short`

## Stop Conditions
- Wrong repo path.
- Dirty status.
- Unexpected branch or remote.
- Commits are not approved for publishing.

## Owner Approval Gates
- Required before every push.

## Constraints
- Do not force push.
- Do not rewrite history.
- Do not auto-push after checks.
