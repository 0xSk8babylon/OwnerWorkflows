# Dependency Provenance Check

## Purpose
Review proposed packages, tools, GitHub Actions, Docker images, external registry dependencies, or installable third-party code before approval.

## When To Use
Use before any install, upgrade, lockfile rewrite, dependency approval, GitHub Action addition, Docker image addition, or third-party tool adoption.

## Procedure / Checklist
1. Confirm the request is review-only until the owner approves installation or lockfile changes.
2. Identify the dependency type: package, tool, GitHub Action, Docker image, external registry dependency, or installable third-party code.
3. Collect need justification:
   - What problem does this dependency solve?
   - Is it required for the approved task?
   - Can the task be done with existing code, standard library, platform features, or already-approved dependencies?
   - What happens if the dependency is rejected?
4. Collect package identity:
   - Exact package, image, action, or tool name.
   - Ecosystem, registry, source, or marketplace.
   - Official repository link, if available.
   - Registry metadata link, if available.
   - Name similarity, typo-squat, and lookalike risk.
   - Whether it is a direct or transitive dependency.
5. Collect version and release timing:
   - Exact proposed version, tag, digest, or commit.
   - Publish date.
   - Recent release history.
   - Suspiciously new package or sudden publish spike.
   - Apply a 14-day cooldown for new, renamed, transferred, or suspicious packages unless the owner explicitly overrides it.
6. Collect maintainer and repository trust evidence:
   - Maintainer continuity.
   - Ownership or maintainer changes.
   - Source repository activity.
   - Issue and PR health.
   - Whether repository metadata matches registry metadata.
   - License visibility.
7. Inspect install behavior:
   - `preinstall`, `install`, or `postinstall` scripts.
   - Binary downloads.
   - Native extensions.
   - Network calls during install.
   - Shell execution.
   - Build hooks.
   - Whether any install behavior needs explicit owner approval.
8. Collect adoption and reputation evidence:
   - Download history or ecosystem usage.
   - Documentation quality.
   - Known users or community signal.
   - Security advisories, if available.
   - Whether the package is obscure for a critical path.
9. Enforce lockfile and approval boundaries:
   - Exact pins are required for direct dependencies.
   - Lockfile diff is required for dependency changes.
   - Dependency changes must be isolated from unrelated changes.
   - No drive-by dependency additions.
   - Owner approval is required before install, upgrade, or lockfile rewrite.
   - Prefer frozen or locked installs after approval.
10. Produce the `Dependency Provenance Review` report and stop before installation unless owner approval is explicit.

## Hard Stops
STOP / BLOCKED if:
- Package name appears typosquatted, misleading, or lookalike.
- Package is newly published, renamed, or recently transferred and no owner override exists.
- Install scripts execute shell or network behavior without approval.
- Registry metadata and source repository do not match.
- Package requests credentials or secrets.
- Dependency is unnecessary or unjustified.
- Lockfile changes appear unrelated.
- Package is security-critical and provenance cannot be verified.

## Owner Approval Gates
- Required before installing, upgrading, regenerating lockfiles, changing Docker images, adding GitHub Actions, or adding third-party tools.
- Required to override the 14-day cooldown.
- Required for install scripts, binary downloads, native extensions, shell execution, or network calls during install.
- Commit and push approval remain separate milestone gates.

## Constraints
- Do not install packages during review.
- Do not query registries when network access is outside approved scope.
- Do not rewrite lockfiles without explicit approval.
- Do not treat "low risk" as installation approval.

## Dependency Provenance Review

- Proposed dependency:
- Need justification:
- Identity check:
- Version/release timing:
- Maintainer/repository trust:
- Install behavior:
- Adoption/reputation:
- Lockfile/approval boundary:
- Risks:
- Recommendation: approve / hold / reject
- Risk classification: low / medium / high / blocked
- Owner decision required:
- Allowed next action:
- Agent must not install until approved:
- Status: APPROVE / HOLD / REJECT / BLOCKED
