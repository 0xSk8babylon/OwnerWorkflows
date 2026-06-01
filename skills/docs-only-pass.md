# Docs-Only Pass

## Purpose
Change documentation while preserving runtime behavior.

## When To Use
Use for README, governance, handoff, checklist, process, or template edits.

## Procedure / Checklist
- Confirm the scope is documentation only.
- Review current diffs.
- Keep status and links consistent.
- Avoid claims that imply unimplemented behavior.
- Run `git diff --check`.
- Report changed files and boundary confirmation.

## Commands
- `git status --short`
- `git diff --check`

## Stop Conditions
- Code, schema, API, data, CI, or deployment changes are required.
- Wording implies unsupported authority, security, compliance, or production readiness.

## Owner Approval Gates
- Required before doctrine changes, publishing, or deleting docs.

## Constraints
- Do not change app code.
- Do not expand architecture or implementation scope.
- Do not publish without approval.
