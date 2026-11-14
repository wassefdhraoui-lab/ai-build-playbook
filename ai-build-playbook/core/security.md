# Security rules

## Secrets
- Never commit keys, tokens, passwords or private emails. Use `.env` (git-ignored) and commit `.env.example` with fake values.
- If a secret was ever committed, treat it as leaked: rotate it. Deleting the commit is not enough.
- Never put secrets in client-side code. Anything in the browser is public.

## Input and output
- Validate every input on the server (type, length, allowed values). Client checks are only for user experience.
- No `eval`, no `new Function`, no `innerHTML`/`dangerouslySetInnerHTML` with user-controlled data.
- Escape output. Use framework defaults.
- Forms: honeypot field, rate limit, size limit, and no stored data unless needed.
- File uploads: check type by content, limit size, never execute, never serve from the app origin.

## Dependencies
- Few and pinned. Prefer well-known packages. Ask before adding one.
- Run `npm audit` (or the equivalent) before every release and read the result.

## Web
- Security headers: Content-Security-Policy, X-Content-Type-Options, Referrer-Policy, frame protection.
- HTTPS only. Cookies (if any): `HttpOnly`, `Secure`, `SameSite`.
- External links: `rel="noopener noreferrer"`.
- Third-party embeds and games from other origins: sandboxed `iframe`.
- No tracking or analytics without a written reason in the brief.

## APIs and services
- Authenticate and authorize every endpoint that changes data.
- Rate limit. Return generic error messages, log details on the server only.
- Keep AI/API keys on the server. Set a spending limit on the provider account.

## Personal data
- Collect the minimum. Say what you collect. Never use real people's data in demos.
