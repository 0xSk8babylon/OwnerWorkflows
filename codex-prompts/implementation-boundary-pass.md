# Implementation Boundary Pass

## Purpose
Verify whether a request changes implementation, contracts, persistence, security, or runtime behavior.

## Use When
Before starting work that might cross from planning into code or operational behavior.

## Scope
Boundary assessment first; implementation only after explicit owner approval.

## Commands / Checklist
- `git status --short`
- Identify affected files and ownership area.
- Classify the change: docs, tests, CI, app code, API, schema, data, security, deployment.
- List required validation commands.
- List compatibility or migration risk.
- Ask for approval if scope crosses into runtime behavior.

## Stop / Report Conditions
- Schema, migration, API, auth, permissions, data, or deployment changes are needed.
- The request could imply legal, financial, safety, compliance, or operational authority.
- Required validation cannot run locally.

## Constraints
- Do not broaden scope silently.
- Do not create hidden runtime behavior.
- Do not add providers, agents, secrets, or integrations unless explicitly approved.
