# Truth Source Review

## Purpose
Classify truth sources before routing a product, doctrine, docs, tests, or implementation decision.

## When To Use
Use when code, tests, docs, doctrine, owner intent, or runtime behavior may conflict.

## Procedure / Checklist
1. Identify the question or decision.
2. Classify whether it concerns intended behavior, actual behavior, verified behavior, documentation, architecture/governance, or product meaning.
3. Inspect relevant evidence.
4. Determine whether sources agree, conflict, reveal a gap, show drift, or indicate intentional evolution.
5. Recommend routing to Product Orchestrator, Doctrine Orchestrator, Repo Stabilization Agent, Implementation Boundary Agent, Docs Governance Agent, or owner decision.
6. Stop before changing doctrine, architecture meaning, code, tests, remotes, or publication state unless explicitly approved.

## Commands
- `git status --short`
- `git diff --name-only`
- `<repo-specific inspection or validation>`

## Stop Conditions
- Source classification is ambiguous.
- Doctrine, architecture meaning, code, tests, remotes, or publication state would change.
- Owner intent is needed to resolve product meaning.

## Owner Approval Gates
- Required before changing product meaning, doctrine, architecture, runtime behavior, tests, remotes, or publishing.
- Commit and push approval remain separate milestone gates.

## Constraints
- Do not treat "safe to commit" or "safe to push" as authorization.
- Do not implement runtime behavior during review.
- Do not force push or rewrite history.
