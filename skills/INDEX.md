# Skills Index

Load one skill for the active procedure. Use agent files first when role boundaries are unclear.

| File | Purpose | When to use | Avoid loading unless needed |
| --- | --- | --- | --- |
| `repo-stabilization.md` | Stabilize repository workflow safely. | CI, validation, git hygiene, branch workflow. | Skip for docs-only work. |
| `safe-push.md` | Verify before a normal push. | Publishing existing local commits. | Skip until owner approves publishing. |
| `session-closeout.md` | Produce final verification and handoff. | End of task or before pausing. | Skip during initial discovery. |
| `docs-only-pass.md` | Keep documentation changes runtime-neutral. | README, governance, templates, checklists. | Skip for runtime work. |
| `implementation-boundary-pass.md` | Identify implementation approval gates. | API, schema, data, security, deployment, or runtime risk. | Skip for confirmed docs-only edits. |
| `add-origin-safely.md` | Add a remote without pushing. | Owner provides a repository URL. | Skip if origin is already correct. |
| `first-push.md` | Publish a new repo branch for the first time. | Clean repo, configured origin, owner-approved first push. | Skip for routine pushes. |
| `truth-source-review.md` | Classify truth sources before routing a decision. | Code, tests, docs, doctrine, owner intent, or runtime behavior may conflict. | Skip when the source of truth is obvious and uncontested. |

Publishing actions require owner approval and a clean, verified repo state.
