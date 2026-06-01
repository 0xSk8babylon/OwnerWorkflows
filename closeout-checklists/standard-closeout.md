# Standard Closeout

## Purpose
Close a work session with clear state and next steps.

## Use When
Any task is complete or paused.

## Scope
Verification and reporting only.

## Commands / Checklist
- `pwd`
- `git status --short`
- `git branch --show-current`
- `git log --oneline -5`
- `git diff --check`
- Report changed or committed files.
- Report validations run.
- Report skipped validation and why.
- Report next safe action.

## Stop / Report Conditions
- Dirty state is unexpected.
- Validation failed.
- Required work remains unclear.

## Constraints
- Do not push as part of standard closeout.
- Do not hide unresolved risks.
- Do not alter files just to make closeout cleaner.
