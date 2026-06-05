# Session Report Emailing

## Purpose
Optionally send an already-generated local session or automation report through an existing configured email sender.

## Boundary
This is reusable workflow doctrine only. It does not configure providers, create credentials, set up domains, add billing, or make email a core product behavior.

## Preconditions
- A local report artifact already exists.
- The owner requested email delivery.
- The project already has an email sender.
- Repo-local `.env` exists for the sending runtime.
- Required environment variables are present after loading `.env`.

## Expected Environment Names
- `RESEND_API_KEY`
- `SESSION_REPORT_FROM`
- `SESSION_REPORT_TO`
- `SESSION_REPORT_USER_AGENT`

## Safe Environment Rules
- `.env` and `.env.*` must not be committed.
- `.env.example` may be committed.
- Secrets must never be printed.
- API keys and tokens must never appear in reports, logs, commits, or prompts.
- Provider test-mode and domain-verification limitations must be reported clearly if encountered.

## Environment Loading
Before any email report send, load repo-local environment variables:

```bash
set -a
source .env
set +a
```

Then verify required variables are present without printing values:

```bash
test -n "${RESEND_API_KEY:-}" &&
test -n "${SESSION_REPORT_FROM:-}" &&
test -n "${SESSION_REPORT_TO:-}" &&
test -n "${SESSION_REPORT_USER_AGENT:-}"
```

Report only variable names that are missing. Do not print variable values.

## Runtime Rules
- Email sending is optional runtime behavior.
- Email failure blocks the email-report delivery request.
- Email failure must be reported with the exact non-secret error.
- Do not run repeated retries that could spam recipients.
- Do not create, edit, expose, rotate, request, or print secrets during the automation run.
- Do not set up external services unless the owner separately approves that work.

## Recommended App Structure
Projects that choose to support email reports may use:

```text
scripts/
send_session_report.py
session_report_email.py

reports/
session-reports/
.gitkeep

.env.example
.gitignore
```

Do not add those files to a project unless the owner approves app-level report delivery work.

## Output Required
- Report file path.
- Subject.
- Delivery command used.
- Success or failure.
- Exact failure error without secrets.
- Missing required variable names, if any.
