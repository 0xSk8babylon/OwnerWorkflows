# Safe Push

## Purpose
Publish local commits only after confirming repository, branch, remote, status, and owner approval.

## Use When
Pushing an existing local branch to a configured remote.

## Scope
Read-only checks until the owner approves the push.

## Commands / Checklist
- `pwd`
- `git status --short`
- `git branch --show-current`
- `git remote -v`
- `git log --oneline -5`
- Confirm the repo path is correct.
- Confirm the current branch is the intended branch.
- Confirm the remote URL is correct.
- Confirm the commits to publish.
- Ask owner approval before pushing.
- After approval: `git push -u origin <branch>`
- After push: `git status --short`

## Stop / Report Conditions
- Wrong repo path.
- Dirty working tree.
- Missing or unexpected remote.
- Unexpected branch.
- Commits are not owner-approved for publishing.

## Constraints
- Do not force push.
- Do not rewrite history.
- Do not push without explicit owner approval.
