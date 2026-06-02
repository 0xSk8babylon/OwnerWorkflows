# Milestone Approval Gates

## Purpose
Clarify when Codex may proceed and when owner approval is required.

## Use When
Reporting commit readiness, push readiness, or boundary-sensitive work.

## Practice
- Approval gates apply at milestone boundaries, not every tiny edit.
- Commit approval and push approval are separate.
- "Safe to commit" means ready for owner review; it does not authorize committing.
- "Safe to push" means ready for owner review; it does not authorize pushing.
- Codex may inspect, edit within approved scope, validate, report progress, and recommend readiness.
- Codex must stop before commit, push, force push, history rewrite, branch/file deletion, remote changes, docs-to-implementation crossing, or doctrine/architecture meaning changes.

## Anti-Patterns
- Treating readiness as approval.
- Combining commit and push approval.
- Asking for approval on every ordinary in-scope edit.
- Crossing from docs to implementation without a new approval gate.

## Validation Or Report Expectations
- State the current milestone, the next gate, and whether approval has been explicitly granted.
