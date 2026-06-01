# CI Change PR

## Purpose
Describe repository validation or workflow changes.

## Use When
Opening a PR for GitHub Actions, test commands, build commands, or workflow infrastructure.

## Scope
CI and repo infrastructure only.

## Commands / Checklist
- Summary:
- Workflow files changed:
- Existing commands used:
- New tooling added: yes/no
- Runtime impact: none unless explicitly described
- Validation run:
- Risks or skipped checks:

## Stop / Report Conditions
- CI requires secrets, credentials, or new external services.
- CI changes app runtime behavior.
- Existing workflow files are replaced without owner approval.

## Constraints
- Do not add secrets.
- Do not force push.
- Do not introduce dependency upgrades unless approved.
