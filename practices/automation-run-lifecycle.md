# Automation Run Lifecycle

## Purpose
Define the reusable lifecycle for owner-controlled temporary automation.

## Lifecycle
1. Owner activates automation.
2. Codex confirms current boundary.
3. Codex performs only safe routine work.
4. Codex hard-stops on prohibited categories.
5. Codex verifies.
6. Codex creates a local commit only if allowed.
7. Codex produces a full report.
8. Owner decides whether to continue, close, push, or escalate.

## Routine Safe Work
- Reading files.
- Inspecting continuity docs.
- Running validation.
- Making additive approved-scope changes.
- Producing report artifacts.

## Closeout
- Use `skills/automation-closeout-report.md`.
- Include final git status.
- State commit and push status explicitly.
- Report failed or skipped verification honestly.
