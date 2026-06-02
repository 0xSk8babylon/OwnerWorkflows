# Push To GitHub

## Context
- Repo path: `<repo-path>`
- Branch: `<branch>`
- Remote: `<remote-name>`
- Expected latest commit: `<commit>`

## Goal
Push clean committed work only after verification and owner approval.

## Scope
Normal push of the approved branch.

## Guardrails
- Do not force push.
- Do not rewrite history.
- Do not push dirty or unreviewed work.
- "Safe to push" means ready for owner review, not permission to push.
- Push approval is separate from commit approval.

## Steps
1. Run `pwd`.
2. Run `git status --short`.
3. Run `git branch --show-current`.
4. Run `git remote -v`.
5. Run `git log --oneline -5`.
6. Confirm repo path, branch, remote, status, and commits with owner.
7. After approval, run `git push origin <branch>`.
8. Run `git status --short`.

## Validation
- Working tree is clean before and after push.
- Remote-visible latest commit matches expected commit.

## Output Required
- Push result.
- Final status.
- Latest remote-visible commit.
