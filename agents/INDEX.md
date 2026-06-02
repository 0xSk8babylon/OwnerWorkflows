# Agents Index

Load one agent file for the role boundary, then load a skill only if procedure detail is needed.

| File | Purpose | When to use | Avoid loading unless needed |
| --- | --- | --- | --- |
| `repo-stabilization-agent.md` | Stabilize git, CI, and validation workflow. | Unknown repo state or workflow repair. | Skip for pure docs or push-only tasks. |
| `github-push-agent.md` | Prepare owner-approved GitHub publishing. | Adding/pushing to a remote. | Skip unless publishing is in scope. |
| `docs-governance-agent.md` | Keep docs/governance changes runtime-neutral. | Docs-only milestones. | Skip for app implementation work. |
| `ci-workflow-agent.md` | Review or add CI using existing commands. | GitHub Actions or validation changes. | Skip when CI is unrelated. |
| `session-closeout-agent.md` | Verify final state and handoff. | End of task or session. | Skip during active implementation. |
| `implementation-boundary-agent.md` | Classify runtime/API/schema/security boundaries. | Ambiguous planning vs implementation work. | Skip for simple read-only checks. |

Do not load every agent by default.
