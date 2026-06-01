# Pre-Push Closeout

## Purpose
Confirm a branch is ready to publish.

## Use When
Before any normal push to a remote repository.

## Scope
Read-only checks until owner approval.

## Commands / Checklist
- `pwd`
- `git status --short`
- `git branch --show-current`
- `git remote -v`
- `git log --oneline -5`
- `git diff --check`
- Confirm commits to publish.
- Confirm remote and branch.
- Ask owner approval to push.

## Stop / Report Conditions
- Dirty working tree.
- Wrong path, branch, or remote.
- Missing validation.
- Owner has not approved publishing.

## Constraints
- Do not force push.
- Do not rewrite history.
- Do not push automatically after checks.
