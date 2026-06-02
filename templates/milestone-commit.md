# Milestone Commit

## Context
- Repo path: `<repo-path>`
- Milestone: `<milestone>`
- Candidate commit message: `<message>`

## Goal
Create a clean milestone commit after review and validation.

## Scope
Only files belonging to the milestone.

## Guardrails
- Do not stage unrelated changes.
- Do not commit failed validation without owner approval.
- Do not push automatically after commit.

## Steps
1. Run `git status --short`.
2. Run `git diff --check`.
3. Run `<repo-specific validation>`.
4. Stage only approved files.
5. Run `git diff --cached --check`.
6. Run `git diff --cached --stat`.
7. Commit with the approved message.
8. Run `git status --short`.
9. Run `git log --oneline -3`.

## Validation
- `git diff --check`
- `git diff --cached --check`
- `<repo-specific validation>`

## Output Required
- Commit hash.
- Files committed.
- Validation performed.
- Risks.
- Recommended next action.
