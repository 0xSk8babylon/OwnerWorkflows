# Repo Stabilization

## Purpose
Stabilize repository workflow or validation without changing application behavior.

## Use When
Repairing CI, branch workflow, remotes, validation commands, or repository hygiene.

## Scope
Repo infrastructure and workflow files only unless the owner approves a broader scope.

## Commands / Checklist
- `pwd`
- `git status --short`
- `git branch --show-current`
- `git remote -v`
- `git log --oneline -10`
- Inspect existing CI and package/test commands.
- Use existing commands only.
- Run `git diff --check`.
- Run configured tests/builds only when already present.

## Stop / Report Conditions
- Validation requires new dependencies or tooling.
- Existing workflow files would need deletion or replacement.
- Runtime app changes appear necessary.

## Constraints
- Do not force push.
- Do not rewrite history.
- Do not add secrets.
- Ask owner approval before publishing, deleting, replacing, or changing branch policy.
