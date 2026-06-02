# Docs vs Implementation

## Purpose
Prevent documentation from silently authorizing runtime behavior.

## Use When
Architecture, process, governance, or roadmap docs mention future capabilities.

## Practice
- Label docs-only work clearly.
- Separate planned, future, and implemented behavior.
- Stop before schemas, APIs, services, providers, agents, deployments, or runtime behavior.
- Use implementation sessions only after explicit owner approval.

## Anti-Patterns
- Letting docs imply a feature exists.
- Treating architecture language as permission to code.
- Mixing docs cleanup with runtime changes.

## Validation Or Report Expectations
- State whether the change is docs-only or implementation.
- Report any wording that could imply unsupported behavior.
