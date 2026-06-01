# Add Origin Safely

## Purpose
Add a GitHub remote without pushing or changing history.

## Use When
Connecting a local repository to a newly created remote repository.

## Scope
Remote configuration only.

## Commands / Checklist
- `pwd`
- `git status --short`
- `git branch --show-current`
- `git remote -v`
- Confirm the owner-provided remote URL.
- Confirm no existing `origin` conflicts.
- Add remote: `git remote add origin <repo-url>`
- Verify: `git remote -v`

## Stop / Report Conditions
- Remote URL is missing, placeholder, or wrong.
- `origin` already exists and differs.
- Current directory is not the intended repo.

## Constraints
- Do not push.
- Do not overwrite an existing remote without owner approval.
- Do not include secrets, tokens, or credentials in the URL.
