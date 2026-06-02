# Commit Isolation

## Purpose
Keep commits clean, reviewable, and reversible.

## Use When
Preparing to stage or commit work.

## Practice
- Stage only files belonging to the milestone.
- Use `git diff --cached --check`.
- Use `git diff --cached --stat`.
- Keep commit messages focused on the milestone.
- Leave unrelated dirty files unstaged.

## Anti-Patterns
- Staging broad directories without checking contents.
- Mixing unrelated generated output.
- Committing owner edits accidentally.

## Validation Or Report Expectations
- Report staged files, validation, commit message, and residual dirty state.
