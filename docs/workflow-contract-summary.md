# Workflow Contract Summary

This document summarizes the core workflow contracts for `agents/`, `orchestrators/`, `templates/`, `practices/`, and `skills/`, plus cross-cutting prompt contract rules.

Supporting surfaces such as `codex-prompts/`, `closeout-checklists/`, `repo-setup/`, `branch-strategy/`, `github-actions/`, `project-templates/`, and the active tracked `pr-templates/` are inventoried in `OWNERWORKFLOWS_INDEX.md` and routed through `OWNERWORKFLOWS_ROUTER.md` when relevant.

## agents/

| File | Purpose (1 line) | Key inputs it expects | Key outputs/actions |
| --- | --- | --- | --- |
| `agents/INDEX.md` | Routes to the one agent needed for the current role boundary. | Task type, role ambiguity, need for procedure detail. | Agent selection guidance and load-minimization rule. |
| `agents/README.md` | Defines agents as reusable repository-operation role definitions. | Need to understand agent folder scope. | Boundary statement: no app code, secrets, or project-specific doctrine. |
| `agents/automation-reporter.md` | Produces read-only owner-visible summaries after long Codex runs. | Codex output, logs, report artifacts, git status, diffs. | Summary, changed files, verification, risks, blockers, next action, optional email-ready report. |
| `agents/ci-workflow-agent.md` | Creates or stabilizes CI using existing project commands. | Package/test/lint/build commands, workflow files, validation needs. | Minimal workflow changes, validation results, runtime impact statement, next safe action. |
| `agents/docs-governance-agent.md` | Updates docs/governance without changing runtime behavior. | Approved docs, wording risks, markdown/whitespace checks. | Changed docs, boundary confirmation, validation, wording risks, commit readiness. |
| `agents/github-push-agent.md` | Prepares owner-approved GitHub publishing. | Repo path, branch, status, remote, commits, owner approval. | Remote/commit summary, normal push result, final status. |
| `agents/implementation-boundary-agent.md` | Classifies whether work crosses into implementation. | Requested files, change type, approval gates, validation needs. | Change classification, boundary risks, required approvals, validation, safe next step. |
| `agents/repo-stabilization-agent.md` | Stabilizes repo workflow, validation, and git hygiene. | Git state, branches, remotes, CI, validation commands, approved stabilization scope. | Files changed, validation performed, risks/blockers, next safe action. |
| `agents/session-closeout-agent.md` | Ends work with clear repo state, validation, and handoff. | Status, branch, remotes, log, validation state, changed files. | Final status, completed work, validation, deferred decisions, next safe action. |
| `agents/stabilization-gatekeeper.md` | Verifies repo state is safe and understandable before closeout. | Git status, changed files, validation record, handoff needs, hard-stop review. | Scope match, git state, verification state, risks/blockers, next safe boundary. |
| `agents/temporary-automation-orchestrator.md` | Runs owner-activated routine automation inside a bounded scope. | Explicit activation, scope, allowed files, forbidden actions, verification, commit permission. | Safe in-scope work, optional approved local commit, local artifacts, required automation report. |

## orchestrators/

| File | Purpose (1 line) | Key inputs it expects | Key outputs/actions |
| --- | --- | --- | --- |
| `orchestrators/INDEX.md` | Routes tasks needing sequencing or governance control. | Task type, governance sensitivity, automation activation status. | Orchestrator choice and truth-source review reminder. |
| `orchestrators/README.md` | Defines orchestrators as sequencing and boundary-control docs. | Need to understand orchestrator folder scope. | Boundary statement: no implementation, approval replacement, publishing, or history rewrite. |
| `orchestrators/automation-run-lifecycle.md` | Sequences temporary automation from activation to owner decision. | Explicit automation scope, boundary, verification route, commit/push permissions. | Lifecycle steps, routing references, stop conditions. |
| `orchestrators/doctrine-orchestrator.md` | Guards governance, meaning, phase, and authority boundaries. | Docs/prompts/templates/agents/skills text, source conflicts, phase claims. | Classification, drift risks, phase risks, required approvals, block/allow recommendation. |
| `orchestrators/product-orchestrator.md` | Sequences product/workflow milestones and routes to agents/skills/templates. | Repo state, milestone type, validation needs, approval gates, truth-source conflicts. | Current state, milestone classification, route, validation, approvals needed, next safe action. |
| `orchestrators/temporary-automation-orchestrator.md` | Coordinates owner-activated routine automation inside a bounded task/phase/milestone. | Repo, branch, task, allowed domains, forbidden actions, verification, commit/push/report flags. | Boundary enforcement, safe automation, hard stops, final report, owner decision boundary. |

## templates/

| File | Purpose (1 line) | Key inputs it expects | Key outputs/actions |
| --- | --- | --- | --- |
| `templates/agent-governance-update.md` | Runs a docs-only agent/orchestrator governance update. | Repo path, governance files, update purpose. | Changed files, governance boundary confirmation, validation, recommended commit message. |
| `templates/architecture-doc-session.md` | Runs a docs-only architecture documentation session. | Repo path, architecture topic, approved docs. | Docs changed, boundary confirmation, validation, recommended commit message. |
| `templates/implementation-session.md` | Guides controlled implementation inside approved boundaries. | Repo path, approved goal, approved files/modules, required validation. | Files and behavior changed, validation, risks/rollback notes, commit readiness. |
| `templates/milestone-commit.md` | Creates a clean milestone commit after review and validation. | Repo path, milestone, candidate message, approved files, validation route. | Commit hash, committed files, validation, risks, recommended next action. |
| `templates/push-to-github.md` | Pushes clean committed work after verification and owner approval. | Repo path, branch, remote, expected latest commit, push approval. | Push result, final status, remote-visible latest commit. |
| `templates/resume-session.md` | Resumes from verified repo state instead of stale chat memory. | Repo path, prior goal, latest known commit, phase, next target. | Completed milestones, dirty state, next target, blockers/owner decisions. |
| `templates/review-before-commit.md` | Reviews changed files and stops for owner commit approval. | Repo path, intended commit scope, candidate message, repo validation commands. | Changed files, scope confirmation, validation, risks/blockers, commit approval request. |
| `templates/stabilization-closeout.md` | Closes a stabilization session with verified state and handoff. | Repo path, completed work, validation target. | Completed work, final status, validation, deferred decisions, recommended next action. |
| `templates/start-new-session.md` | Starts a clean Codex session from verified repository state. | Repo path, expected branch, current goal, known guardrails. | Repo/branch/status/remotes/commits, confirmed scope and guardrails, next safe action. |

## practices/

| File | Purpose (1 line) | Key inputs it expects | Key outputs/actions |
| --- | --- | --- | --- |
| `practices/INDEX.md` | Routes to the one practice needed for the operating question. | Scope question, git risk, docs/runtime ambiguity, automation status. | Practice selection guidance. |
| `practices/README.md` | Defines practices as reusable operating doctrine. | Need to understand practice folder scope. | Boundary statement: no app code, secrets, credentials, private doctrine, or repo URLs. |
| `practices/automation-run-lifecycle.md` | Defines owner-controlled temporary automation lifecycle. | Activation, safe routine work, verification, commit allowance. | Lifecycle, safe-work list, closeout expectations. |
| `practices/boundary-before-execution.md` | Confirms the operating boundary before automated file changes. | Repo, branch, scope, continuity docs, dirty state, prohibited actions, verification, commit/push permission. | Planned route before edits; stop if scope, verification, or permissions are unclear. |
| `practices/commit-isolation.md` | Keeps commits clean, reviewable, and reversible. | Milestone files, staged diff, validation, commit message, residual dirty state. | Scope-limited staging/reporting and cached diff checks. |
| `practices/context-routing.md` | Reduces token load by loading the smallest useful context first. | Session/task type, navigation/index files, relevant references. | Context route taken and follow-up context used. |
| `practices/deferred-decisions.md` | Keeps unresolved choices visible without forcing premature action. | Decision, reason deferred, needed evidence/approval. | Deferred decision, owner input needed, next safe action. |
| `practices/docs-vs-implementation.md` | Prevents docs from silently authorizing runtime behavior. | Docs/architecture/process claims, future capabilities, implementation pressure. | Docs-only/runtime classification and overclaim risks. |
| `practices/lockfile-integrity.md` | Treats lockfiles as the approved dependency install boundary. | Dependency changes, lockfile diffs, package manager output, frozen install needs. | Lockfile integrity review, drift classification, blockers, owner decision route. |
| `practices/local-first-push-later.md` | Separates local commit quality from public publishing. | Local validation, owner commit approval, branch/remote/latest commits, push approval. | Local latest commit, remote target, clean status, explicit push approval status. |
| `practices/milestone-approval-gates.md` | Clarifies where owner approval is required. | Milestone, next gate, readiness state, boundary-sensitive actions. | Current gate, explicit approval status, required stop points. |
| `practices/milestone-boundaries.md` | Keeps work grouped into clear reviewable milestones. | Milestone sentence, in-scope file groups, validation risk. | Scope, changed files, validation, risks, next safe action. |
| `practices/negative-constraints.md` | Makes prohibited actions explicit so safe work can proceed. | Must-not-change items, allowed scope, risk areas. | Constraints touched/avoided or requiring approval. |
| `practices/non-destructive-git.md` | Preserves history, branches, and owner work. | Command intent, branch state, remote state, destructive risk. | Approval requirement and safe git route. |
| `practices/owner-controlled-escalation.md` | Separates routine automation from high-risk owner decisions. | Scope clarity, escalation trigger, high-risk work category. | Stop reason, completed work, remaining safe work, owner decision needed separately. |
| `practices/owner-intent-vs-implementation.md` | Keeps product meaning distinct from current runtime behavior. | Owner intent, code behavior, docs/tests evidence, divergence. | Evidence summary, divergence classification, recommended route. |
| `practices/phase-sequencing.md` | Orders planning, implementation, validation, commit, and push. | Current phase, milestone boundaries, validation status, approval needs. | Current phase, next gate, required approval, validation status. |
| `practices/repo-state-inspection.md` | Starts from verified repo facts. | Path, branch, remotes, latest commits, dirty files. | Repo state report and dirty-state risk. |
| `practices/session-closeout.md` | Ends work with clean state, validation, and handoff. | Branch, status, remotes, commits, validation, changed/committed files. | Status, validation, risks, deferred decisions, owner-review readiness. |
| `practices/truth-source-classification.md` | Classifies evidence before changing docs/doctrine/tests/implementation. | Owner intent, doctrine, code, tests, docs, runtime behavior, conflicts/gaps/drift. | Source finding, conflict/gap/drift/evolution classification, recommended route. |
| `practices/validation-by-scope.md` | Matches validation effort to change risk and blast radius. | Change type, risk, available tests/checks, skipped checks. | Validation run/skipped and scope justification. |

## skills/

| File | Purpose (1 line) | Key inputs it expects | Key outputs/actions |
| --- | --- | --- | --- |
| `skills/INDEX.md` | Routes to the one procedural skill needed for the active task. | Active procedure, role clarity, publishing status. | Skill selection guidance and publishing prerequisite reminder. |
| `skills/README.md` | Defines skills as reusable deterministic workflow checklists. | Need to understand skill folder scope. | Boundary statement: generic workflow infrastructure only. |
| `skills/add-origin-safely.md` | Adds an owner-provided remote without pushing. | Repo path, status, branch, remotes, owner-provided URL. | Remote added/verified or stop reason. |
| `skills/automation-closeout-report.md` | Produces the required final report for automation runs. | Scope, changed files, verification, approvals, hard-stop review, git state. | Standard automation report with honest verification, push status, risks, next boundary. |
| `skills/docs-only-pass.md` | Changes documentation while preserving runtime behavior. | Docs scope, current diffs, wording/status/link consistency. | Changed files, runtime-neutral confirmation, diff check, stop on implementation drift. |
| `skills/first-push.md` | Publishes a new repo branch for the first time after approval. | Clean repo, branch, remote, recent commits, owner approval. | First push result and verified status. |
| `skills/hard-stop-boundary-enforcement.md` | Stops automation before prohibited high-risk actions. | Proposed action, automation context, hard-stop category. | Stop report with trigger, authority boundary, completed work, files touched, owner decision needed. |
| `skills/implementation-boundary-pass.md` | Identifies runtime/operational authority crossings. | Request classification, affected files, validation, compatibility/migration risk. | Approval gates, stop conditions, implementation boundary decision. |
| `skills/local-milestone-commit.md` | Creates an approved local milestone commit without pushing. | Explicit commit permission, concrete scope, verification route, inspected working tree. | Commit hash, files committed, validation, final status, push status not pushed. |
| `skills/repo-stabilization.md` | Stabilizes repo workflow without changing app behavior. | Repo path/status/branch/remotes, workflow/validation files, approved stabilization scope. | Stabilization edits, validation, stop on overlap/dependency/destructive needs. |
| `skills/safe-push.md` | Pushes only owner-approved commits from verified state. | Repo path, status, branch, remotes, recent commits, explicit push approval. | Normal push result or stop reason; no force/history rewrite. |
| `skills/scoped-automation-activation.md` | Validates temporary automation activation scope. | Repo, branch, phase/task, allowed domains, forbidden actions, verification, commit/push/report flags. | Activated boundary, verification route, commit/push permissions, first safe action. |
| `skills/secret-boundary-enforcement.md` | Prevents automation from adding, exposing, requesting, or committing secrets. | Changed files, env/provider config, commands that may print credentials. | Secret-boundary stop report or confirmation that only safe examples are involved. |
| `skills/session-closeout.md` | Ends a session with verified state and concise handoff. | Repo state, branch, remotes, commits, diff check, validation, changed files. | Validation, risks, changed files, next safe action, owner-review readiness. |
| `skills/session-report-emailing.md` | Sends an existing local report through an already configured email sender. | Existing report artifact, owner email request, configured sender, `.env`, required env vars. | Delivery command/result, missing variable names, non-secret failure details. |
| `skills/truth-source-review.md` | Classifies truth sources before routing product/doctrine/docs/tests/implementation decisions. | Decision question, relevant evidence, source conflicts, repo diffs/validation. | Agreement/conflict/gap/drift/evolution finding and route recommendation. |

## Workflow Contract

### Restore prompt must include

- Repo path, expected branch, current goal, latest known commit, current phase, and next target.
- Known guardrails, allowed files/domains, and forbidden actions.
- Required initial checks: `pwd`, `git status --short`, current branch, remotes when relevant, and recent commits.
- Dirty-state handling: classify dirty files as in-scope, out-of-scope, or blockers before editing.
- Instruction to resume from current repository state, not stale chat memory, and not to overwrite user changes.
- Commit and push permissions stated explicitly, with push treated as separate approval.

### Implementation prompt must include

- Repo path, approved implementation goal, approved files/modules, and concrete milestone scope.
- Required validation commands and rollback/risk expectations.
- Whether schemas, APIs, auth, data, providers, telemetry, deployments, dependencies, or migrations are explicitly in scope.
- Guardrails against silent scope expansion, unrelated refactors, secrets, and docs-to-runtime authorization drift.
- Requirement to inspect relevant files before editing, run validation, run `git diff --check`, and review before commit.
- Explicit commit permission status and explicit push prohibition unless separately approved.

### Closeout prompt must include

- Repo path, completed work summary, validation target, and whether continuity docs or reports are required.
- Required final checks: `pwd`, `git status --short`, branch, remotes when relevant, recent commits, and `git diff --check` when a diff exists.
- Changed or committed files, validation run/skipped with reasons, risks/blockers, deferred decisions, and next safe action.
- Explicit statement that "safe to commit" and "safe to push" mean owner-review readiness only.
- Commit hash if created, final dirty state, and push status.
- For automation runs, the full `Automation Report` sections from `skills/automation-closeout-report.md`.

### Approval gates that must be respected

- Scope expansion.
- Runtime, schema, API, auth, data, security, provider, agent, telemetry, dependency, migration, or deployment work.
- Doctrine, governance, architecture meaning, product meaning, permissions, provenance, or phase-promotion changes.
- Remote creation/change, branch policy changes, destructive git, history rewrite, branch/file deletion, and force push.
- Commit milestones: readiness is not approval; commit only after explicit owner approval.
- Push or publishing milestones: separate explicit owner approval is required after commit approval.
- External services, secrets, credentials, billing, production deployment, and email/provider setup.

### Hard-stop rules that override everything

- During temporary automation, stop and report if a hard-stop action appears necessary; do not ask to bypass it inside the run.
- Hard stops include git push, migrations, auth/security/permission enforcement changes, deleting files, doctrine rewrites, scope changes, unrelated repo changes, external services or secrets, broad refactors, billing changes, production deployment, destructive commands, force push, and history rewrite.
- Stop when scope, verification route, commit permission, or push permission is unclear.
- Stop before printing, adding, editing, requesting, rotating, or committing secrets; never commit `.env` files or expose credentials.
- Stop before treating docs as implementation approval or treating code behavior as doctrine/product meaning.
- Stop before changing remotes, publishing, or committing/pushing without explicit owner approval.
- Failed or skipped validation must be reported honestly; do not claim verification that did not run.
