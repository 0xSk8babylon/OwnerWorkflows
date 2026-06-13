# OwnerWorkflows Router

Use this router after reading `AGENTS.md` and `OWNERWORKFLOWS_INDEX.md`.

Templates are a selection library, not a prompt bundle. Select the smallest safe workflow set for the classified task. When scope is uncertain, default to read-only inspection, report the classification, and ask the owner before editing or crossing boundaries.

Each route below lists recommended files that currently exist. If an ideal specialized file is absent, the route says `not currently present`.

## Universal Routing Rules

1. Classify the task before loading task-specific docs.
2. Load one agent when a role boundary is needed.
3. Load one skill when a deterministic procedure is needed.
4. Load only practices that constrain the active risk.
5. Load one template only when the task shape matches it.
6. Use one closeout checklist at the end.
7. Stop and ask the owner before any hard-stop boundary.

## Routes

### Docs-Only Changes

| Field | Route |
| --- | --- |
| Recommended agent | `agents/docs-governance-agent.md` |
| Recommended skill | `skills/docs-only-pass.md` |
| Required practices | `practices/docs-vs-implementation.md`, `practices/validation-by-scope.md`, `practices/commit-isolation.md` |
| Recommended template | `templates/agent-governance-update.md` or `templates/architecture-doc-session.md` when the task is architecture docs |
| Closeout checklist | `closeout-checklists/standard-closeout.md` |
| Hard stops | Runtime code, API, schema, data, migration, deploy, auth/security/permission changes, doctrine rewrite, unrelated repos, deletion, destructive commands. |
| Stop and ask owner | If docs imply new runtime behavior, change doctrine meaning, require code changes, or touch files outside approved docs scope. |

### Backend Implementation Prompts

| Field | Route |
| --- | --- |
| Recommended agent | `agents/implementation-boundary-agent.md` |
| Recommended skill | `skills/implementation-boundary-pass.md` |
| Required practices | `practices/docs-vs-implementation.md`, `practices/validation-by-scope.md`, `practices/truth-source-classification.md`, `practices/owner-intent-vs-implementation.md` when product meaning may be affected |
| Recommended template | `templates/implementation-session.md` |
| Closeout checklist | `closeout-checklists/standard-closeout.md` |
| Hard stops | Migrations, schema/API/data/security/auth/permission changes, dependencies, deploys, secrets, broad refactors unless explicitly approved. |
| Stop and ask owner | If the requested prompt would authorize implementation without approved files, validation route, migration stance, compatibility risk, or data/security boundary. |

### Frontend/UI Implementation Prompts

| Field | Route |
| --- | --- |
| Recommended agent | `agents/implementation-boundary-agent.md` |
| Recommended skill | `skills/implementation-boundary-pass.md` |
| Required practices | `practices/validation-by-scope.md`, `practices/owner-intent-vs-implementation.md`, `practices/docs-vs-implementation.md` |
| Recommended template | `templates/implementation-session.md` |
| Closeout checklist | `closeout-checklists/standard-closeout.md` |
| Hard stops | Auth/permission changes, data-flow changes, API/schema changes, deploys, dependencies, broad refactors, unrelated repos. |
| Stop and ask owner | If UI work requires backend/API changes, new providers, new dependencies, unapproved design doctrine, or runtime authority beyond the approved UI scope. |

### Repo Stabilization

| Field | Route |
| --- | --- |
| Recommended agent | `agents/repo-stabilization-agent.md` |
| Recommended skill | `skills/repo-stabilization.md` |
| Required practices | `practices/repo-state-inspection.md`, `practices/non-destructive-git.md`, `practices/validation-by-scope.md`, `practices/commit-isolation.md` |
| Recommended template | `templates/stabilization-closeout.md` for closeout, or `codex-prompts/repo-stabilization.md` in Codex |
| Closeout checklist | `closeout-checklists/standard-closeout.md` |
| Hard stops | Force push, history rewrite, deleting files/branches, dependency changes, secrets, deploys, broad refactors, runtime behavior changes. |
| Stop and ask owner | If stabilization requires destructive git, package installs, dependency changes, CI secret configuration, runtime code changes, or unclear dirty state. |

### Architecture Map Generation

| Field | Route |
| --- | --- |
| Recommended agent | `agents/docs-governance-agent.md` |
| Recommended skill | `skills/docs-only-pass.md` |
| Required practices | `practices/context-routing.md`, `practices/truth-source-classification.md`, `practices/docs-vs-implementation.md`, `practices/validation-by-scope.md` |
| Recommended template | `templates/architecture-doc-session.md` |
| Closeout checklist | `closeout-checklists/standard-closeout.md` |
| Hard stops | Runtime changes, doctrine rewrites, authority/compliance/production-readiness claims, broad refactors, unrelated repos. |
| Stop and ask owner | If mapping requires interpreting private doctrine, resolving product meaning conflicts, or updating code to match docs. |

### Session Report Email

| Field | Route |
| --- | --- |
| Recommended agent | `agents/automation-reporter.md` |
| Recommended skill | `skills/session-report-emailing.md` |
| Required practices | `practices/owner-controlled-escalation.md`, `practices/negative-constraints.md` |
| Recommended template | `codex-prompts/send-automation-report.md` |
| Closeout checklist | `closeout-checklists/standard-closeout.md` |
| Hard stops | Creating external services, changing secrets, printing env values, repeated retries, deploys, auth changes. |
| Stop and ask owner | If no local report artifact exists, email configuration is missing, required env vars are absent, or setup would require external provider work. |

### Dependency/Provenance Review

| Field | Route |
| --- | --- |
| Recommended agent | `agents/implementation-boundary-agent.md` |
| Recommended skill | `skills/truth-source-review.md`; specialized dependency/provenance skill is not currently present |
| Required practices | `practices/truth-source-classification.md`, `practices/validation-by-scope.md`, `practices/negative-constraints.md` |
| Recommended template | not currently present |
| Closeout checklist | `closeout-checklists/standard-closeout.md` |
| Hard stops | Dependency installs/upgrades, provider changes, external services, secrets, security/permission changes, deploys. |
| Stop and ask owner | If review would require installing packages, changing lockfiles, contacting external services, or making security claims beyond inspected evidence. |

### Lockfile/Package Safety

| Field | Route |
| --- | --- |
| Recommended agent | `agents/repo-stabilization-agent.md` |
| Recommended skill | Specialized lockfile/package safety skill is not currently present; use `skills/repo-stabilization.md` only for repo-state and validation boundaries |
| Required practices | `practices/repo-state-inspection.md`, `practices/validation-by-scope.md`, `practices/non-destructive-git.md`, `practices/negative-constraints.md` |
| Recommended template | not currently present |
| Closeout checklist | `closeout-checklists/standard-closeout.md` |
| Hard stops | Package installs, dependency upgrades, lockfile rewrites, external registries, scripts with side effects, deploys, security/permission changes unless approved. |
| Stop and ask owner | If the task requires installing, updating, regenerating, or deleting package manager files. |

### Milestone Commit / Checkpoint Review

| Field | Route |
| --- | --- |
| Recommended agent | `agents/session-closeout-agent.md` |
| Recommended skill | `skills/local-milestone-commit.md` only when commit is explicitly approved |
| Required practices | `practices/commit-isolation.md`, `practices/milestone-approval-gates.md`, `practices/local-first-push-later.md`, `practices/validation-by-scope.md` |
| Recommended template | `templates/review-before-commit.md`, then `templates/milestone-commit.md` if owner approves commit |
| Closeout checklist | `closeout-checklists/standard-closeout.md` |
| Hard stops | Committing without explicit approval, staging unrelated changes, failed validation without owner decision, push after commit. |
| Stop and ask owner | If changed files include unrelated dirty work, commit message/scope is unclear, validation failed, or approval is only phrased as readiness. |

### Pre-Push Review

| Field | Route |
| --- | --- |
| Recommended agent | `agents/github-push-agent.md` |
| Recommended skill | `skills/safe-push.md` |
| Required practices | `practices/local-first-push-later.md`, `practices/milestone-approval-gates.md`, `practices/non-destructive-git.md`, `practices/repo-state-inspection.md` |
| Recommended template | `templates/push-to-github.md` |
| Closeout checklist | `closeout-checklists/pre-push-closeout.md` |
| Hard stops | Push without explicit approval, force push, history rewrite, unclear branch/remote/status/commit range, dirty unrelated state. |
| Stop and ask owner | If branch, remote, expected latest commit, push approval, or working tree state is unclear. |

### Compromise/Security Response

| Field | Route |
| --- | --- |
| Recommended agent | `agents/implementation-boundary-agent.md` |
| Recommended skill | `skills/secret-boundary-enforcement.md`; specialized compromise response skill is not currently present |
| Required practices | `practices/negative-constraints.md`, `practices/owner-controlled-escalation.md`, `practices/non-destructive-git.md` |
| Recommended template | not currently present |
| Closeout checklist | `closeout-checklists/standard-closeout.md` |
| Hard stops | Printing secrets, rotating credentials, changing auth/security/permissions, external services, destructive cleanup, deploys, broad refactors. |
| Stop and ask owner | If incident response requires provider access, credential rotation, secret revocation, permission changes, legal/compliance claims, or destructive cleanup. |

### Closeout/Final Report

| Field | Route |
| --- | --- |
| Recommended agent | `agents/session-closeout-agent.md`; use `agents/stabilization-gatekeeper.md` when state is uncertain |
| Recommended skill | `skills/session-closeout.md`; use `skills/automation-closeout-report.md` for automation runs |
| Required practices | `practices/session-closeout.md`, `practices/validation-by-scope.md`, `practices/milestone-approval-gates.md` |
| Recommended template | `templates/stabilization-closeout.md` for stabilization, `codex-prompts/session-closeout.md` for Codex, or not currently present for generic final report template |
| Closeout checklist | `closeout-checklists/standard-closeout.md` unless preparing to push, then `closeout-checklists/pre-push-closeout.md` |
| Hard stops | Hiding dirty state, claiming skipped validation, pushing, destructive commands, continuing into new scope. |
| Stop and ask owner | If final status is blocked by unclear dirty state, failed validation, missing approval, or a request to continue into another milestone. |

## Owner Hard Stops

Stop and report if the task requires crossing any of these boundaries:

- no git push unless explicitly approved by owner
- no migrations
- no auth, security, or permission changes
- no deleting files
- no doctrine rewrites
- no unrelated repos
- no external services or secrets
- no deploys
- no broad refactors
- no destructive commands

If a hard stop is required to complete the task, do not route around it. Report the blocking boundary, completed safe work, files inspected, and the owner decision needed.
