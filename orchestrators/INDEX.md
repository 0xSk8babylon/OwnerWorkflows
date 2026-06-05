# Orchestrators Index

Load one orchestrator when a task needs sequencing or governance boundary control.

| File | Purpose | When to use | Avoid loading unless needed |
| --- | --- | --- | --- |
| `product-orchestrator.md` | Sequence product/workflow milestones and route to agents, skills, or templates. | Multi-step project motion, milestone planning, workflow ordering. | Skip for simple single-command tasks. |
| `doctrine-orchestrator.md` | Guard doctrine, governance, phase, and meaning boundaries. | Architecture, governance, permissions, provenance, phase boundaries, or product meaning. | Skip for routine git status checks. |
| `temporary-automation-orchestrator.md` | Coordinate owner-activated routine automation inside a bounded task, phase, or milestone. | Owner explicitly activates temporary automation. | Skip unless activation is explicit. |
| `automation-run-lifecycle.md` | Sequence activation, boundary check, safe work, verification, optional local commit, and report. | Planning or closing a temporary automation run. | Skip for ordinary sessions. |

Use `skills/truth-source-review.md` before either orchestrator resolves conflicts among owner intent, doctrine, code, tests, docs, or runtime behavior.

Product motion must not bypass doctrine review when governance or meaning boundaries are involved.
