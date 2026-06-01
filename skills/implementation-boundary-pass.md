# Implementation Boundary Pass

## Purpose
Identify whether work crosses into runtime implementation or operational authority.

## When To Use
Use before changes involving app code, schemas, APIs, persistence, security, integrations, or deployment.

## Procedure / Checklist
- Classify the request: docs, CI, tests, app code, API, schema, data, security, deployment.
- Identify affected files.
- Identify required validation.
- Identify compatibility and migration risk.
- Ask for approval before implementation scope begins.

## Commands
- `git status --short`
- `git diff --name-only`

## Stop Conditions
- Runtime behavior changes without approval.
- Schema, API, auth, data, or deployment changes without approval.
- Required validation cannot run.

## Owner Approval Gates
- Required before runtime, schema, API, data, security, provider, agent, telemetry, or deployment changes.

## Constraints
- Do not broaden scope silently.
- Do not treat docs as implementation approval.
- Do not add secrets or integrations without approval.
