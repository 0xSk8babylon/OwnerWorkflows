# Implementation Session

## Context
- Repo path: `<repo-path>`
- Approved implementation goal: `<goal>`
- Approved files or modules: `<files>`
- Required validation: `<commands>`

## Goal
Make controlled implementation changes within approved boundaries.

## Scope
Only the approved implementation target.

## Guardrails
- Do not broaden file scope silently.
- Do not change schemas, APIs, auth, data, deployments, or dependencies unless approved.
- Preserve rollback awareness and avoid unrelated refactors.

## Steps
1. Run initial git state checks.
2. Inspect relevant files before editing.
3. Make scoped changes.
4. Run required tests/builds.
5. Run `git diff --check`.
6. Use `templates/review-before-commit.md` before committing.

## Validation
- `<repo-specific tests/builds>`
- `git diff --check`

## Output Required
- Files changed.
- Behavior changed.
- Validation results.
- Risks and rollback notes.
- Commit readiness.
