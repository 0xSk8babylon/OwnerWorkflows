# First Push

## Purpose
Publish a new repository branch to GitHub for the first time.

## Use When
A local repo has an initial commit and a configured remote.

## Scope
Publishing the intended branch only after verification and owner approval.

## Commands / Checklist
- `pwd`
- `git status --short`
- `git branch --show-current`
- `git remote -v`
- `git log --oneline -5`
- Confirm branch should be `main` or another owner-approved default.
- Confirm remote URL and account.
- Confirm commits to publish.
- Ask owner approval before pushing.
- After approval: `git push -u origin <branch>`
- Verify: `git status --short`

## Stop / Report Conditions
- Branch is not the intended default branch.
- Working tree is dirty.
- Remote is missing or incorrect.
- Authentication is unavailable.

## Constraints
- Do not force push.
- Do not rewrite history.
- Do not publish before owner approval.
