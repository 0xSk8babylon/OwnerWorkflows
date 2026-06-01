# Branch Naming

## Purpose
Use predictable branch names that communicate intent.

## Use When
Creating branches for normal development.

## Scope
Naming only; does not define merge or release policy.

## Commands / Checklist
- Use `feature/<short-scope>` for implementation work.
- Use `fix/<short-scope>` for stabilization or bug fixes.
- Use `docs/<short-scope>` for documentation-only changes.
- Use `ci/<short-scope>` for workflow and validation changes.
- Keep scope short, lowercase, and hyphen-separated.
- Before creating: `git status --short`.
- Create: `git switch -c <type>/<short-scope>`.

## Stop / Report Conditions
- Working tree has unrelated dirty files.
- Branch name hides runtime, docs, or CI scope.

## Constraints
- Do not delete branches without owner approval.
- Do not reuse broad names like `changes`, `updates`, or `work`.
- Do not rewrite history to rename published branches without owner approval.
