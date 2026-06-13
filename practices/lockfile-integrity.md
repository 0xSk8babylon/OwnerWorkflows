# Lockfile Integrity

## Purpose
Treat lockfiles as the enforcement boundary between owner-approved dependency intent and what actually installs.

## Use When
Reviewing dependency changes, lockfile changes, package manager output, dependency drift, frozen installs, or any task where manifests and lockfiles may change.

## Practice
- Direct dependencies must use exact versions where the ecosystem supports it.
- Floating ranges such as `^`, `~`, `>=`, `*`, `latest`, `main`, `master`, or unpinned Git refs are unapproved delegation of owner authority.
- Exceptions to exact pins require explicit owner approval and written rationale.
- Lockfiles record the resolved dependency graph.
- Lockfile changes are security-relevant and must not be treated as noise.
- Lockfile drift can introduce unapproved code even when manifest changes look small.
- Lockfile changes must be reviewed before acceptance.
- After approval, use frozen or locked install commands where available:
  - `npm ci`
  - `pnpm install --frozen-lockfile`
  - `yarn install --frozen-lockfile`
  - `poetry install` with an existing lockfile
  - `uv sync --frozen`
  - `pip install` with hashed requirements where applicable
- If the ecosystem lacks a frozen install option, state that explicitly.

## Lockfile Diff Classification
- In-scope: lockfile changes directly caused by the approved dependency/version change.
- Out-of-scope: lockfile changes unrelated to the approved task, even if harmless-looking.
- Blocker: lockfile changes that introduce unexpected packages, registry/source changes, install scripts, binary/native packages, credential access, or unclear provenance.

## Review Requirements
A lockfile review must summarize:
- Changed lockfiles.
- Direct dependency changes.
- Transitive dependency changes.
- Added packages.
- Removed packages.
- Changed versions.
- Registry/source changes.
- Packages with install scripts.
- Binary/native package additions.
- Any unexpected lockfile rewrite.

## Separation Of Concerns
- Dependency and lockfile changes must be isolated from unrelated feature, formatting, or docs changes.
- No drive-by lockfile rewrites.
- No formatting-only task should rewrite lockfiles.
- No unrelated package manager migration should occur during a normal dependency task.

## Relationship To Dependency Provenance
- New dependency approval must use `skills/dependency-provenance-check.md` first.
- Lockfile integrity review happens after an approved dependency change creates or modifies a lockfile.
- Provenance asks whether the dependency should be allowed.
- Lockfile integrity asks whether the resolved installed graph matches what was approved.

## Hard Stops
STOP / BLOCKED if:
- Lockfile changes include unrelated packages.
- Lockfile changes include registry/source changes without approval.
- Lockfile changes include install scripts, binary downloads, or native packages without approval.
- Manifest and lockfile disagree.
- Lockfile is deleted or regenerated without approval.
- Floating dependency ranges are introduced without owner approval.
- Package manager migration occurs without approval.
- Lockfile changes cannot be explained.

## Validation Or Report Expectations
Use this report format:

### Lockfile Integrity Review

- Changed lockfiles:
- Approved dependency scope:
- Direct dependency changes:
- Transitive dependency changes:
- Added packages:
- Removed packages:
- Registry/source changes:
- Install scripts / binary / native changes:
- In-scope changes:
- Out-of-scope changes:
- Blockers:
- Recommendation:
- Owner decision required:
- Status: PASS / NEEDS FIX / BLOCKED
