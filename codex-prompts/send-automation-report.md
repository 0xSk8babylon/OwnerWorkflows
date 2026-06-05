# Send Automation Report

Use this prompt to send an already-generated local report artifact through an existing configured email sender.

```text
Send an automation report email.

Required inputs:

- local report file path:
- subject:

Rules:

- use existing env vars only
- before sending, load repo-local env vars with:
  set -a
  source .env
  set +a
- verify required vars are present without printing values
- do not print secrets
- do not create or edit secrets
- do not set up an email provider
- do not configure billing, domains, DNS, or production delivery
- email failure is a blocker for the email-report delivery request
- no repeated retries that could spam recipients
- paste the exact non-secret error on failure
- print clear success/failure
```

## Expected Environment Names
- `RESEND_API_KEY`
- `SESSION_REPORT_FROM`
- `SESSION_REPORT_TO`
- `SESSION_REPORT_USER_AGENT`

## Failure Handling
Treat delivery failure as a blocker for the email-report delivery request. Paste the exact non-secret error and do not retry repeatedly.
