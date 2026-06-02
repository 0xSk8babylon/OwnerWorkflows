# Repo State Inspection

## Purpose
Start from facts instead of assumptions.

## Use When
Beginning work, switching repos, resuming after interruption, or preparing to publish.

## Practice
- Confirm `pwd`.
- Check `git status --short`.
- Check current branch and remotes.
- Inspect recent commits.
- Identify dirty files before editing.

## Anti-Patterns
- Working in the wrong repo.
- Ignoring pre-existing dirty files.
- Assuming remote state without fetching or checking.

## Validation Or Report Expectations
- Report path, branch, status, remotes, latest commits, and any dirty-state risk.
