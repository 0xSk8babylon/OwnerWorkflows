# Session Start

## Purpose
Start a Codex session from verified local state.

## Use When
Beginning work in any repository.

## Scope
Discovery only. Do not edit files until the task boundary is clear.

## Commands / Checklist
- `pwd`
- `git status --short`
- `git branch --show-current`
- `git remote -v`
- `git log --oneline -5`
- Identify the requested repo and confirm it is not a different project.
- Identify dirty files and whether they predate the session.

## Stop / Report Conditions
- Wrong repository or unexpected path.
- Dirty files that overlap the requested scope.
- Missing git repository.
- User asks for a plan before edits.

## Constraints
- Do not rewrite history.
- Do not delete branches.
- Do not push.
- Do not modify files before reporting initial state.
