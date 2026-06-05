# Navigation

Load the smallest relevant file first. Use follow-up files only when the active task needs more procedural detail.

## Approval Gates

- Approval gates apply at milestone boundaries, not every file edit.
- Within an approved scope, Codex may inspect, edit, validate, report progress, and recommend commit or push readiness.
- "Safe to commit" means ready for owner review; it does not authorize committing unless owner approval is explicit.
- "Safe to push" means ready for owner review; it does not authorize pushing unless owner approval is explicit.
- Owner approval is required before commit and again before push.
- Stop before committing, pushing, force pushing, rewriting history, deleting branches/files, changing remotes, crossing from docs into implementation, or changing doctrine/architecture meaning.

| Situation | Load first | Optional follow-up |
| --- | --- | --- |
| Product/workflow sequencing | `orchestrators/product-orchestrator.md` | `orchestrators/doctrine-orchestrator.md` when meaning or governance is involved |
| Doctrine/governance boundary review | `orchestrators/doctrine-orchestrator.md` | `agents/docs-governance-agent.md` |
| Starting a repo session | `codex-prompts/session-start.md` | `skills/session-closeout.md` |
| Stabilizing unknown repo state | `agents/repo-stabilization-agent.md` | `skills/repo-stabilization.md` |
| Docs-only milestone | `agents/docs-governance-agent.md` | `skills/docs-only-pass.md` |
| Safe push | `agents/github-push-agent.md` | `skills/safe-push.md` |
| Add a remote origin | `repo-setup/add-origin-safely.md` | `skills/add-origin-safely.md` |
| First push | `repo-setup/first-push.md` | `skills/first-push.md` |
| Session closeout | `agents/session-closeout-agent.md` | `skills/session-closeout.md` |
| CI workflow review | `agents/ci-workflow-agent.md` | `skills/repo-stabilization.md` |
| Implementation boundary control | `agents/implementation-boundary-agent.md` | `skills/implementation-boundary-pass.md` |
| Temporary automation activation | `orchestrators/temporary-automation-orchestrator.md` | `skills/scoped-automation-activation.md` |
| Temporary automation lifecycle | `orchestrators/automation-run-lifecycle.md` | `practices/automation-run-lifecycle.md` |
| Automation hard-stop review | `skills/hard-stop-boundary-enforcement.md` | `practices/owner-controlled-escalation.md` |
| Automation closeout report | `skills/automation-closeout-report.md` | `agents/stabilization-gatekeeper.md` |
| Automation run summary | `agents/automation-reporter.md` | `codex-prompts/send-automation-report.md` only when email is requested |
| Secret boundary review | `skills/secret-boundary-enforcement.md` | `practices/negative-constraints.md` |
| Defining a milestone boundary | `practices/milestone-boundaries.md` | `templates/milestone-commit.md` |
| Deciding docs-only vs implementation | `practices/docs-vs-implementation.md` | `skills/implementation-boundary-pass.md` |
| Classifying truth sources | `practices/truth-source-classification.md` | `skills/truth-source-review.md` |
| Owner intent vs implementation conflict | `practices/owner-intent-vs-implementation.md` | `orchestrators/product-orchestrator.md` |
| Closing out a session | `practices/session-closeout.md` | `agents/session-closeout-agent.md` |
| Inspecting repo state | `practices/repo-state-inspection.md` | `codex-prompts/session-start.md` |
| Sequencing project phases | `practices/phase-sequencing.md` | `orchestrators/product-orchestrator.md` |
| Tracking deferred decisions | `practices/deferred-decisions.md` | `templates/stabilization-closeout.md` |
| Isolating commits | `practices/commit-isolation.md` | `templates/review-before-commit.md` |
| Avoiding destructive git | `practices/non-destructive-git.md` | `skills/repo-stabilization.md` |
| Validating by scope | `practices/validation-by-scope.md` | `skills/repo-stabilization.md` |
| Reducing token/context load | `practices/context-routing.md` | Folder `INDEX.md` files |
| Clarifying owner approval before commit/push | `practices/milestone-approval-gates.md` | `templates/milestone-commit.md` |
| Long-running session templates | `templates/start-new-session.md` | The matching file in `templates/` |
| Architecture docs session | `templates/architecture-doc-session.md` | `skills/docs-only-pass.md` |
| Implementation session | `templates/implementation-session.md` | `skills/implementation-boundary-pass.md` |
| Local milestone commit | `skills/local-milestone-commit.md` | `templates/milestone-commit.md` |
| Milestone commit | `templates/milestone-commit.md` | `templates/review-before-commit.md` |
| PR description | `pr-templates/INDEX.md` | The matching PR template |

Publishing actions require owner approval. Do not force push, rewrite history, or publish from ambiguous repo state.
