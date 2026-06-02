# PR Templates Index

Load only the template that matches the pull request type.

| File | Purpose | When to use | Avoid loading unless needed |
| --- | --- | --- | --- |
| `docs-change.md` | Describe documentation-only changes. | Docs, governance, process, or templates. | Skip if runtime behavior changed. |
| `ci-change.md` | Describe workflow or validation changes. | GitHub Actions, tests, builds, CI commands. | Skip for app-only work. |
| `implementation-change.md` | Describe app or service changes. | Runtime code, API, UI, persistence, or tests. | Skip for docs-only changes. |
| `stabilization-change.md` | Describe narrow fixes or risk reduction. | Bug fixes, workflow stabilization, validation repair. | Skip for broad feature work. |

PR text must not include secrets, credentials, or unsupported implementation claims.
