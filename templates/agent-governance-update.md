# Agent Governance Update

## Context
- Repo path: `<repo-path>`
- Governance file(s): `<files>`
- Update purpose: `<purpose>`

## Goal
Update agent or orchestrator governance without implementing runtime behavior.

## Scope
Governance docs, agent instructions, routing notes, or operating procedures.

## Guardrails
- Do not add runtime code, services, agents, tools, providers, or deployments.
- Do not include secrets, credentials, private keys, or tokens.
- Do not overstate current automation capability.

## Steps
1. Run `git status --short`.
2. Review current governance docs.
3. Apply concise wording or routing updates.
4. Check for duplication and scope drift.
5. Run `git diff --check`.

## Validation
- `git diff --check`
- Governance remains documentation-only.

## Output Required
- Files changed.
- Governance boundary confirmation.
- Validation results.
- Recommended commit message.
