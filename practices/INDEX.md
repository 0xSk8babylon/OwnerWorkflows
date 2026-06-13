# Practices Index

Load one practice file for the operating question at hand.

| File | Purpose | Use when |
| --- | --- | --- |
| `milestone-boundaries.md` | Define what belongs in a milestone. | Scope or commit shape is unclear. |
| `docs-vs-implementation.md` | Separate documentation from runtime work. | Docs may imply behavior changes. |
| `session-closeout.md` | End a session with clear state. | Pausing or completing work. |
| `repo-state-inspection.md` | Start from verified repo state. | Beginning or resuming work. |
| `phase-sequencing.md` | Order project phases safely. | Planning multi-step work. |
| `deferred-decisions.md` | Track decisions without forcing them. | A choice is not ready. |
| `commit-isolation.md` | Keep commits milestone-sized. | Preparing a commit. |
| `non-destructive-git.md` | Avoid unsafe git operations. | Any branch/history action is possible. |
| `local-first-push-later.md` | Commit locally before publishing. | GitHub visibility is not immediate. |
| `validation-by-scope.md` | Match validation to change risk. | Choosing tests/checks. |
| `lockfile-integrity.md` | Treat lockfiles as the approved dependency install boundary. | Reviewing lockfile changes, dependency drift, frozen installs, or package manager output. |
| `context-routing.md` | Reduce token load by routing first. | Deciding what to read. |
| `negative-constraints.md` | Make prohibited actions explicit. | Scope needs guardrails. |
| `milestone-approval-gates.md` | Clarify commit/push approvals. | Reporting readiness or stopping at gates. |
| `owner-intent-vs-implementation.md` | Keep product meaning and current behavior distinct. | Owner intent and implementation may diverge. |
| `truth-source-classification.md` | Classify owner intent, doctrine, code, tests, docs, runtime behavior, gaps, drift, and evolution. | Sources disagree or routing is unclear. |
| `boundary-before-execution.md` | Confirm repo, branch, scope, dirty state, prohibited actions, verification, and commit/push permission before automation. | Starting an automated run. |
| `owner-controlled-escalation.md` | Separate routine safe automation from high-risk owner decisions. | A run may need escalation or has unclear scope. |
| `automation-run-lifecycle.md` | Define activation, safe work, hard stops, verification, optional local commit, and owner decision boundary. | Running or reviewing temporary automation. |
