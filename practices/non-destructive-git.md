# Non-Destructive Git

## Purpose
Preserve history, branches, and owner work.

## Use When
Any command might alter history, branches, remotes, or files.

## Practice
- Prefer inspection before mutation.
- Fetch before integrating remote changes.
- Merge normally unless owner approves another strategy.
- Stop before destructive commands.

## Anti-Patterns
- Force pushing.
- Rewriting history without approval.
- Deleting branches or files to simplify status.
- Reverting changes you did not make.

## Validation Or Report Expectations
- Report command intent, branch state, remote state, and whether owner approval is required before continuing.
