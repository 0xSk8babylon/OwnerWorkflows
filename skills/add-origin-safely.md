# Add Origin Safely

## Purpose
Connect a local repository to an owner-provided remote without pushing.

## When To Use
Use when a repository needs a GitHub `origin`.

## Procedure / Checklist
- Confirm `pwd`.
- Run `git status --short`.
- Run `git branch --show-current`.
- Run `git remote -v`.
- Confirm the owner-provided URL is not a placeholder.
- Add `origin` only if no conflicting remote exists.
- Verify remotes after adding.

## Commands
- `git remote add origin <repo-url>`
- `git remote -v`

## Stop Conditions
- URL is missing, placeholder, or includes credentials.
- `origin` already exists and differs.
- Wrong repo path.

## Owner Approval Gates
- Required before adding a new remote.
- Required before replacing or changing an existing remote.
- Required before any push.

## Constraints
- Do not push.
- Do not include secrets, tokens, or credentials in remote URLs.
- Do not overwrite remotes without approval.
