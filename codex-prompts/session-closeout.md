# Session Closeout

## Purpose
End a session with clean state, clear validation, and safe next actions.

## Use When
After completing a milestone, commit, workflow repair, or investigation.

## Scope
Reporting and final verification.

## Commands / Checklist
- `pwd`
- `git status --short`
- `git branch --show-current`
- `git remote -v`
- `git log --oneline -5`
- `git diff --check`
- Report changed files or committed files.
- Report validation performed and skipped.
- Report deferred decisions.

## Stop / Report Conditions
- Working tree is dirty unexpectedly.
- A push, destructive command, or history rewrite would be needed.
- Validation failed or could not run.

## Constraints
- Do not push during closeout unless separately approved.
- Do not hide dirty state.
- Do not mark work complete if required validation is unresolved.
