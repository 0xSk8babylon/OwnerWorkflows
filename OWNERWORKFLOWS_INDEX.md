# OwnerWorkflows Index

This is the machine-readable inventory for OwnerWorkflows. Use it after `AGENTS.md` and before task-specific workflow docs.

Status values:

- `active`: available for routing as a current workflow file
- `reference`: useful background or examples, not a default execution route
- `deprecated`: retained only for history
- `unknown`: purpose, availability, or owner classification is unclear

Categories:

- `entrypoint`
- `agent`
- `skill`
- `practice`
- `template`
- `closeout checklist`
- `github action workflow doc`
- `project/reference doc`
- `example/reference only`
- `unknown/requires owner classification`

## Major Folders

| Folder | Category | Status | When to use | When not to use |
| --- | --- | --- | --- | --- |
| `agents/` | agent | active | Select one role boundary for the task. | Do not load every agent by default. |
| `skills/` | skill | active | Select one procedural checklist for deterministic work. | Do not use skills to expand owner-approved scope. |
| `practices/` | practice | active | Select operating constraints for scope, approval, validation, or routing. | Do not treat practices as implementation approval. |
| `templates/` | template | active | Select one task-shaped prompt or report template. | Do not load the whole folder as a prompt bundle. |
| `closeout-checklists/` | closeout checklist | active | Select one end-of-task checklist. | Do not use closeout to hide unresolved risk. |
| `github-actions/` | github action workflow doc | reference | Inspect reusable CI notes. | Do not change GitHub Actions behavior without approval. |
| `codex-prompts/` | template | active | Select one Codex-specific prompt when running a matching Codex workflow. | Do not treat Codex prompts as universal startup context. |
| `orchestrators/` | project/reference doc | active | Use one orchestrator for sequencing or governance boundary control. | Do not use orchestrators to bypass owner approval. |
| `repo-setup/` | skill | active | Use for remote setup, first push, or safe push procedures. | Do not use unless publishing or remote setup is in scope. |
| `branch-strategy/` | project/reference doc | reference | Use for branch naming or default-branch decisions. | Do not change branch policy without owner approval. |
| `project-templates/` | example/reference only | reference | Inspect starter structure notes for future repositories. | Do not apply to an existing project by default. |
| `docs/` | project/reference doc | unknown | Local worktree has untracked docs requiring owner classification. | Do not route to untracked docs as canonical GitHub workflow source. |
| `pr-templates/` | template | unknown | Tracked in git history but currently deleted from the local worktree. | Do not route to local PR templates until owner resolves availability. |

## Root Files

| Path | Category | Status | When to use | When not to use |
| --- | --- | --- | --- | --- |
| `AGENTS.md` | entrypoint | active | First file for all LLM and agent harnesses. | Do not skip it when using this repo as workflow source. |
| `OWNERWORKFLOWS_INDEX.md` | entrypoint | active | Inventory available workflow docs before routing. | Do not treat it as task procedure by itself. |
| `OWNERWORKFLOWS_ROUTER.md` | entrypoint | active | Route a classified task to the smallest safe workflow set. | Do not use it to invent missing files. |
| `README.md` | project/reference doc | reference | Understand repo purpose and folder structure. | Do not use as the only operating instruction. |
| `NAVIGATION.md` | project/reference doc | active | Quick human-readable routing and approval-gate overview. | Do not override `AGENTS.md` or owner hard stops. |

## Agents

| Path | Category | Status | When to use | When not to use |
| --- | --- | --- | --- | --- |
| `agents/INDEX.md` | agent | active | Choose one agent file. | Do not load all agents. |
| `agents/README.md` | project/reference doc | reference | Understand the agent folder scope. | Do not use as a role boundary. |
| `agents/automation-reporter.md` | agent | active | Summarize a completed run or report artifact. | Do not use during implementation. |
| `agents/ci-workflow-agent.md` | agent | active | Review or add CI using existing commands. | Do not add secrets, deploy keys, or unapproved tooling. |
| `agents/docs-governance-agent.md` | agent | active | Keep docs/governance changes runtime-neutral. | Do not use for app implementation. |
| `agents/github-push-agent.md` | agent | active | Prepare owner-approved GitHub publishing. | Do not push without explicit approval. |
| `agents/implementation-boundary-agent.md` | agent | active | Classify runtime, API, schema, security, or data boundaries. | Do not skip for ambiguous implementation requests. |
| `agents/repo-stabilization-agent.md` | agent | active | Stabilize git, CI, validation, or workflow state. | Do not use for pure docs-only work unless repo state is unclear. |
| `agents/session-closeout-agent.md` | agent | active | Verify final state and produce handoff. | Do not use while active implementation is still underway. |
| `agents/stabilization-gatekeeper.md` | agent | active | End-of-run safety review for uncertain closeout state. | Do not use as permission to continue work. |
| `agents/temporary-automation-orchestrator.md` | agent | active | Run owner-activated routine automation inside a bounded scope. | Do not use unless automation is explicitly activated. |

## Skills

| Path | Category | Status | When to use | When not to use |
| --- | --- | --- | --- | --- |
| `skills/INDEX.md` | skill | active | Choose one procedural skill. | Do not load all skills. |
| `skills/README.md` | project/reference doc | reference | Understand the skills folder scope. | Do not use as a checklist. |
| `skills/add-origin-safely.md` | skill | active | Add an owner-provided remote without pushing. | Do not overwrite remotes without approval. |
| `skills/automation-closeout-report.md` | skill | active | Produce a final automation report. | Do not claim verification that did not run. |
| `skills/docs-only-pass.md` | skill | active | Make documentation-only changes. | Do not change app code or runtime behavior. |
| `skills/first-push.md` | skill | active | First push after clean state and owner approval. | Do not use for routine pushes. |
| `skills/hard-stop-boundary-enforcement.md` | skill | active | Stop before prohibited high-risk actions. | Do not use it to request bypasses inside automation. |
| `skills/implementation-boundary-pass.md` | skill | active | Identify implementation approval gates. | Do not treat docs as implementation approval. |
| `skills/local-milestone-commit.md` | skill | active | Create an owner-approved local commit without pushing. | Do not commit without explicit approval. |
| `skills/repo-stabilization.md` | skill | active | Repair repo workflow, validation, or git hygiene. | Do not change app behavior without approval. |
| `skills/safe-push.md` | skill | active | Push owner-approved commits from verified state. | Do not force push or auto-push. |
| `skills/scoped-automation-activation.md` | skill | active | Validate temporary automation activation. | Do not infer automation from ordinary approval. |
| `skills/secret-boundary-enforcement.md` | skill | active | Prevent secrets from being exposed, requested, or committed. | Do not print or modify secret values. |
| `skills/session-closeout.md` | skill | active | End a session with verified state and concise handoff. | Do not alter files just to make status cleaner. |
| `skills/session-report-emailing.md` | skill | active | Send an existing report through existing email configuration. | Do not set up services or expose env values. |
| `skills/truth-source-review.md` | skill | active | Classify conflicts among owner intent, docs, code, tests, and doctrine. | Do not implement runtime behavior during review. |

## Practices

| Path | Category | Status | When to use | When not to use |
| --- | --- | --- | --- | --- |
| `practices/INDEX.md` | practice | active | Choose one practice for the operating question. | Do not load all practices. |
| `practices/README.md` | project/reference doc | reference | Understand practice folder scope. | Do not use as task procedure. |
| `practices/automation-run-lifecycle.md` | practice | active | Run or review temporary automation. | Do not use for ordinary sessions unless automation is active. |
| `practices/boundary-before-execution.md` | practice | active | Confirm repo, branch, scope, dirty state, and approvals before automation. | Do not skip when automated file changes begin. |
| `practices/commit-isolation.md` | practice | active | Keep commits milestone-sized and reviewable. | Do not stage unrelated changes. |
| `practices/context-routing.md` | practice | active | Reduce context load before selecting docs. | Do not load directories by habit. |
| `practices/deferred-decisions.md` | practice | active | Track unresolved choices without forcing them. | Do not resolve owner decisions by inference. |
| `practices/docs-vs-implementation.md` | practice | active | Separate docs-only work from runtime work. | Do not let docs imply unimplemented behavior. |
| `practices/local-first-push-later.md` | practice | active | Separate local commit quality from publishing. | Do not treat push readiness as approval. |
| `practices/milestone-approval-gates.md` | practice | active | Clarify commit and push approval boundaries. | Do not combine commit and push approval. |
| `practices/milestone-boundaries.md` | practice | active | Define reviewable milestone scope. | Do not turn a milestone into a broad refactor. |
| `practices/negative-constraints.md` | practice | active | Make prohibited actions explicit. | Do not use constraints as a checklist of things to touch. |
| `practices/non-destructive-git.md` | practice | active | Avoid unsafe git operations. | Do not rewrite history or delete branches/files. |
| `practices/owner-controlled-escalation.md` | practice | active | Stop when routine work becomes high-risk owner decision. | Do not escalate by changing scope yourself. |
| `practices/owner-intent-vs-implementation.md` | practice | active | Keep owner intent distinct from current behavior. | Do not convert current behavior into doctrine. |
| `practices/phase-sequencing.md` | practice | active | Order planning, implementation, validation, commit, and push. | Do not skip gates for speed. |
| `practices/repo-state-inspection.md` | practice | active | Start from verified repo facts. | Do not rely on stale chat memory. |
| `practices/session-closeout.md` | practice | active | End work with status, validation, and next action. | Do not hide dirty state or skipped checks. |
| `practices/truth-source-classification.md` | practice | active | Classify evidence and conflicts before changing meaning. | Do not blend conflicting sources into new doctrine. |
| `practices/validation-by-scope.md` | practice | active | Match validation to change risk. | Do not overclaim skipped validation. |

## Templates

| Path | Category | Status | When to use | When not to use |
| --- | --- | --- | --- | --- |
| `templates/agent-governance-update.md` | template | active | Docs-only agent or orchestrator governance update. | Do not add runtime tools, providers, or deployments. |
| `templates/architecture-doc-session.md` | template | active | Architecture documentation session. | Do not change runtime code, APIs, schemas, or data. |
| `templates/implementation-session.md` | template | active | Controlled implementation inside approved boundaries. | Do not broaden scope silently. |
| `templates/milestone-commit.md` | template | active | Owner-approved milestone commit. | Do not push after commit. |
| `templates/push-to-github.md` | template | active | Owner-approved push after verification. | Do not use without explicit push approval. |
| `templates/resume-session.md` | template | active | Resume from verified repo state. | Do not overwrite existing dirty work. |
| `templates/review-before-commit.md` | template | active | Review changed files before owner commit approval. | Do not treat readiness as approval. |
| `templates/stabilization-closeout.md` | template | active | Close a stabilization session. | Do not continue into a new scope. |
| `templates/start-new-session.md` | template | active | Start a clean session from verified state. | Do not edit before scope and state are confirmed. |

## Closeout Checklists

| Path | Category | Status | When to use | When not to use |
| --- | --- | --- | --- | --- |
| `closeout-checklists/INDEX.md` | closeout checklist | active | Choose the correct closeout checklist. | Do not load both by default. |
| `closeout-checklists/README.md` | project/reference doc | reference | Understand closeout checklist scope. | Do not use as final closeout procedure. |
| `closeout-checklists/pre-push-closeout.md` | closeout checklist | active | Before owner-approved push. | Do not push automatically after checks. |
| `closeout-checklists/standard-closeout.md` | closeout checklist | active | Normal completion or pause. | Do not use when preparing to push. |

## Codex Prompts

| Path | Category | Status | When to use | When not to use |
| --- | --- | --- | --- | --- |
| `codex-prompts/INDEX.md` | template | active | Choose one Codex-specific prompt. | Do not load all prompts as startup context. |
| `codex-prompts/README.md` | project/reference doc | reference | Understand Codex prompt folder scope. | Do not use as task procedure. |
| `codex-prompts/activate-temporary-automation.md` | template | active | Activate bounded temporary automation. | Do not use unless automation is explicit. |
| `codex-prompts/closeout-automation-run.md` | template | active | Close and report an automation run. | Do not continue into a new scope. |
| `codex-prompts/docs-only-pass.md` | template | active | Run a docs-only Codex pass. | Do not modify app code. |
| `codex-prompts/implementation-boundary-pass.md` | template | active | Assess implementation boundary risk. | Do not implement before approval. |
| `codex-prompts/repo-stabilization.md` | template | active | Stabilize repo workflow. | Do not change app runtime behavior. |
| `codex-prompts/save-temporary-automation-orchestrator.md` | template | active | Save temporary automation workflow docs. | Do not duplicate existing doctrine. |
| `codex-prompts/send-automation-report.md` | template | active | Send an existing local report when owner requests email. | Do not set up external services or print secrets. |
| `codex-prompts/session-closeout.md` | template | active | Close a Codex session. | Do not push during closeout. |
| `codex-prompts/session-start.md` | template | active | Start from verified local state. | Do not edit files before reporting initial state. |

## Orchestrators

| Path | Category | Status | When to use | When not to use |
| --- | --- | --- | --- | --- |
| `orchestrators/INDEX.md` | project/reference doc | active | Choose one orchestrator. | Do not load all orchestrators. |
| `orchestrators/README.md` | project/reference doc | reference | Understand orchestrator folder scope. | Do not use as sequencing procedure. |
| `orchestrators/automation-run-lifecycle.md` | project/reference doc | active | Sequence temporary automation. | Do not use for ordinary tasks. |
| `orchestrators/doctrine-orchestrator.md` | project/reference doc | active | Guard doctrine, governance, phase, and meaning boundaries. | Do not rewrite doctrine without owner approval. |
| `orchestrators/product-orchestrator.md` | project/reference doc | active | Sequence multi-step product or workflow milestones. | Do not bypass doctrine or approval gates. |
| `orchestrators/temporary-automation-orchestrator.md` | project/reference doc | active | Coordinate owner-activated routine automation. | Do not use unless explicitly activated. |

## Repository Setup And Branch Strategy

| Path | Category | Status | When to use | When not to use |
| --- | --- | --- | --- | --- |
| `repo-setup/INDEX.md` | skill | active | Choose one repo setup workflow. | Do not push automatically. |
| `repo-setup/README.md` | project/reference doc | reference | Understand repo setup scope. | Do not use as exact push procedure. |
| `repo-setup/add-origin-safely.md` | skill | active | Add an owner-provided origin. | Do not push or overwrite remotes without approval. |
| `repo-setup/first-push.md` | skill | active | Publish a new repo branch for the first time. | Do not use for established branches. |
| `repo-setup/safe-push.md` | skill | active | Verify and push existing commits safely. | Do not use before branch, remote, status, and approval are clear. |
| `branch-strategy/README.md` | project/reference doc | reference | Understand branch strategy docs. | Do not change branch policy from README alone. |
| `branch-strategy/branch-naming.md` | project/reference doc | reference | Choose or review branch naming. | Do not rename branches without owner approval. |
| `branch-strategy/main-vs-master.md` | project/reference doc | reference | Review default branch naming. | Do not change defaults without owner approval. |

## GitHub Actions And Project References

| Path | Category | Status | When to use | When not to use |
| --- | --- | --- | --- | --- |
| `github-actions/README.md` | github action workflow doc | reference | Inspect reusable GitHub Actions notes. | Do not add secrets or change CI behavior without approval. |
| `project-templates/README.md` | example/reference only | reference | Review future project skeleton notes. | Do not apply to an existing repo by default. |

## PR Templates Availability Note

The following files are tracked in git history but were deleted in the local worktree during this index update. Treat them as `unknown` until the owner resolves the working tree state.

| Path | Category | Status | When to use | When not to use |
| --- | --- | --- | --- | --- |
| `pr-templates/INDEX.md` | template | unknown | Route to one PR template after availability is restored. | Do not route to it while deleted locally. |
| `pr-templates/README.md` | project/reference doc | unknown | Understand PR template scope after availability is restored. | Do not use while deleted locally. |
| `pr-templates/ci-change.md` | template | unknown | CI-change PR description after availability is restored. | Do not use while deleted locally. |
| `pr-templates/docs-change.md` | template | unknown | Docs-change PR description after availability is restored. | Do not use while deleted locally. |
| `pr-templates/implementation-change.md` | template | unknown | Implementation-change PR description after availability is restored. | Do not use while deleted locally. |
| `pr-templates/stabilization-change.md` | template | unknown | Stabilization PR description after availability is restored. | Do not use while deleted locally. |

## Local Untracked Markdown

The following file was present as untracked local markdown during this index update. Treat it as non-canonical until the owner commits or otherwise classifies it.

| Path | Category | Status | When to use | When not to use |
| --- | --- | --- | --- | --- |
| `docs/workflow-contract-summary.md` | unknown/requires owner classification | unknown | Only after owner classifies it as part of the canonical GitHub workflow source. | Do not route to it while it remains untracked local context. |

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
