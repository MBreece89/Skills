# Security

## Secrets and Credentials
- Never hardcode secrets, API keys, passwords, or tokens in source code.
- Use environment variables or a secrets manager for sensitive values.
- Add sensitive file patterns to `.gitignore` (e.g., `.env`, `*.key`, `*.pem`).

## Input Validation
- Validate and sanitize all user input on both client and server.
- Use parameterized queries / prepared statements — never concatenate user input into SQL.
- Encode output to prevent XSS (HTML-escape, URL-encode as appropriate).
- Validate file uploads: check type, size, and content — not just the extension.

## Authentication and Authorization
- Use established libraries/frameworks for auth — do not roll your own crypto.
- Apply the principle of least privilege for all access controls.
- Validate permissions on every request server-side, regardless of UI state.
- Use secure session management (HttpOnly, Secure, SameSite cookies).

## Network and Transport
- Enforce HTTPS everywhere; redirect HTTP to HTTPS.
- Set proper security headers: `Content-Security-Policy`, `X-Content-Type-Options`, `Strict-Transport-Security`, `X-Frame-Options`.
- Configure CORS restrictively — allow only known origins.

## Dependencies
- Keep dependencies up to date; monitor for known vulnerabilities (CVEs).
- Pin dependency versions in production builds.
- Audit new dependencies before adding them (popularity, maintenance, license).

## Error Handling
- Never expose stack traces, internal paths, or system details in error responses.
- Log security events (failed logins, privilege escalations) for monitoring.
- Fail securely — deny by default when authorization is uncertain.

## Code Review
- Treat security-sensitive changes with extra scrutiny.
- Look for: hardcoded secrets, missing input validation, broken access controls, injection vectors.

