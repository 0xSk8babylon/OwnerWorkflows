# Docs-Only Pass

## Purpose
Make documentation changes without changing runtime behavior.

## Use When
Updating README files, handoffs, governance notes, process docs, or architecture summaries.

## Scope
Documentation files only.

## Commands / Checklist
- `git status --short`
- Review diffs before editing.
- Confirm docs do not imply unimplemented behavior.
- Keep links and status language consistent.
- Run `git diff --check`.
- Report changed files.

## Stop / Report Conditions
- Docs require code, schema, API, migration, or runtime changes.
- Wording implies authority, security, compliance, production readiness, or implementation that does not exist.
- The requested edit touches private or project-specific material outside scope.

## Constraints
- Do not modify app code.
- Do not add implementation instructions beyond the approved documentation boundary.
- Do not publish or push without owner approval.
