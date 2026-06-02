# Repo Setup Index

Load one setup file for the exact publishing step. Do not push automatically.

| File | Purpose | When to use | Avoid loading unless needed |
| --- | --- | --- | --- |
| `add-origin-safely.md` | Add an owner-provided remote. | Local repo has no correct `origin`. | Skip if no URL is provided. |
| `first-push.md` | Publish a new repo branch for the first time. | Clean repo, configured remote, owner approval. | Skip for established branches. |
| `safe-push.md` | Verify and push existing commits safely. | Routine owner-approved push. | Skip until branch, remote, status, and commits are confirmed. |

All publishing actions require owner approval. Force push is prohibited.
