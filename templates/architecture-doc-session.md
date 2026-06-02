# Architecture Doc Session

## Context
- Repo path: `<repo-path>`
- Architecture topic: `<topic>`
- Approved docs: `<files>`

## Goal
Run a docs-only architecture session without implying implementation approval.

## Scope
Architecture documentation, links, status notes, and governance wording.

## Guardrails
- Do not change runtime code, schemas, APIs, services, providers, agents, telemetry, deployment, or data.
- Do not claim authority, compliance, production readiness, or operational control.
- Do not expand scope beyond approved docs.

## Steps
1. Run `git status --short`.
2. Read only the relevant architecture docs.
3. Update approved docs with concise, source-aware wording.
4. Check for implementation drift and overclaims.
5. Run `git diff --check`.

## Validation
- `git diff --check`
- Scope remains docs/governance only.

## Output Required
- Docs changed.
- Boundary confirmation.
- Validation results.
- Recommended commit message.
