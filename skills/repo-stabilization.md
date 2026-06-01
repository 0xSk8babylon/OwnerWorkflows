# Repo Stabilization

## Purpose
Repair or stabilize repository workflow without changing app behavior.

## When To Use
Use for CI, validation, branch workflow, remote, or git hygiene work.

## Procedure / Checklist
- Confirm `pwd`.
- Run `git status --short`.
- Run `git branch --show-current`.
- Run `git remote -v`.
- Inspect existing workflow and validation files.
- Use existing commands before adding tooling.
- Run `git diff --check`.

## Commands
- `git log --oneline -10`
- `find .github -maxdepth 3 -type f -print`
- `git diff --check`

## Stop Conditions
- Wrong repo.
- Dirty files overlap scope.
- Existing workflows require deletion or replacement.
- New dependencies are needed.

## Owner Approval Gates
- Publishing.
- Destructive changes.
- Branch policy changes.
- Dependency or tool additions.

## Constraints
- Do not force push.
- Do not rewrite history.
- Do not add secrets.
- Do not change app runtime behavior without approval.
