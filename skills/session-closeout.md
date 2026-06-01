# Session Closeout

## Purpose
End a session with verified state and a concise handoff.

## When To Use
Use after commits, investigation, stabilization, or before pausing.

## Procedure / Checklist
- Confirm `pwd`.
- Run `git status --short`.
- Run `git branch --show-current`.
- Run `git remote -v`.
- Run `git log --oneline -5`.
- Run `git diff --check`.
- Report validation, changed files, risks, and next safe action.

## Commands
- `git status --short`
- `git diff --check`

## Stop Conditions
- Unexpected dirty state.
- Validation failure.
- Required work remains unresolved.

## Owner Approval Gates
- Required before push, deletion, history rewrite, or branch cleanup.

## Constraints
- Do not push during closeout unless separately approved.
- Do not hide skipped validation.
- Do not modify files just to make status cleaner.
