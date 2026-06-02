# Navigation

Load the smallest relevant file first. Use follow-up files only when the active task needs more procedural detail.

| Situation | Load first | Optional follow-up |
| --- | --- | --- |
| Starting a repo session | `codex-prompts/session-start.md` | `skills/session-closeout.md` |
| Stabilizing unknown repo state | `agents/repo-stabilization-agent.md` | `skills/repo-stabilization.md` |
| Docs-only milestone | `agents/docs-governance-agent.md` | `skills/docs-only-pass.md` |
| Safe push | `agents/github-push-agent.md` | `skills/safe-push.md` |
| Add a remote origin | `repo-setup/add-origin-safely.md` | `skills/add-origin-safely.md` |
| First push | `repo-setup/first-push.md` | `skills/first-push.md` |
| Session closeout | `agents/session-closeout-agent.md` | `skills/session-closeout.md` |
| CI workflow review | `agents/ci-workflow-agent.md` | `skills/repo-stabilization.md` |
| Implementation boundary control | `agents/implementation-boundary-agent.md` | `skills/implementation-boundary-pass.md` |
| Long-running session templates | `templates/start-new-session.md` | The matching file in `templates/` |
| Architecture docs session | `templates/architecture-doc-session.md` | `skills/docs-only-pass.md` |
| Implementation session | `templates/implementation-session.md` | `skills/implementation-boundary-pass.md` |
| Milestone commit | `templates/milestone-commit.md` | `templates/review-before-commit.md` |
| PR description | `pr-templates/INDEX.md` | The matching PR template |

Publishing actions require owner approval. Do not force push, rewrite history, or publish from ambiguous repo state.
