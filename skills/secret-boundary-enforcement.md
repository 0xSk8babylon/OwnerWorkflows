# Secret Boundary Enforcement

## Purpose
Prevent automation from creating, exposing, requesting, or committing secrets.

## Automation Must Never
- Add secrets.
- Edit secrets.
- Expose secrets.
- Rotate secrets.
- Request secrets mid-run.
- Commit `.env` files.
- Print API keys, tokens, credentials, cookies, private keys, or provider secrets.
- Set up external providers without explicit owner approval.

## Required Checks
- Inspect changed files for `.env`, `.env.*`, credentials, keys, tokens, and provider config.
- Treat `.env.example` as documentation only and never include real values.
- Report secret-related files as blocked unless they are explicit safe examples.

## Stop Conditions
- A command would print a secret.
- A required next step needs a credential.
- A provider setup or domain verification step is needed.
- A changed file could contain live credentials.

## Report When Stopped
- Secret boundary encountered.
- Files or commands involved.
- Work completed before the stop.
- Owner action needed outside the automation run.
