# Review Before Commit

## Context
- Repo path: `<repo-path>`
- Intended commit scope: `<scope>`
- Commit message candidate: `<message>`

## Goal
Review changed files before committing and wait for owner approval.

## Scope
Only files approved for the milestone.

## Guardrails
- Do not stage unrelated files.
- "Safe to commit" means ready for owner review, not permission to commit.
- Do not commit until owner approves.
- Do not push as part of review.

## Steps
1. Run `git status --short`.
2. Run `git diff --name-only`.
3. Review diffs for scope, secrets, generated noise, and unintended behavior.
4. Run validation commands already appropriate for the repo.
5. Run `git diff --check`.

## Validation
- `git diff --check`
- `<repo-specific validation>`

## Output Required
- Files changed.
- Scope confirmation.
- Validation results.
- Risks or blockers.
- Ask for commit approval.
