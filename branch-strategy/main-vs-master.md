# Main vs Master

## Purpose
Choose and preserve a stable default branch name.

## Use When
Initializing a repo, renaming a local branch, or preparing a first push.

## Scope
Default branch policy and local branch naming.

## Commands / Checklist
- Check current branch: `git branch --show-current`.
- Check all branches: `git branch -a`.
- Prefer `main` for new repositories unless the owner chooses otherwise.
- Rename local default before first push: `git branch -M main`.
- Confirm: `git branch --show-current`.
- Push only after owner approval.

## Stop / Report Conditions
- Branch is already published.
- Remote default branch already exists.
- Other collaborators depend on the old branch name.

## Constraints
- Do not delete `master` or any branch without owner approval.
- Do not rewrite history.
- Do not force push branch renames.
