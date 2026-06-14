# Security Policy — SparkleClean

## Architecture
SparkleClean is a **static website** (HTML/CSS/vanilla JS) with:
- No backend server, no application code running on a server
- No database
- No API keys or secrets in the codebase
- No user accounts, sessions, or stored personal data
- No third-party scripts (only Google Fonts CSS)

This eliminates entire classes of attacks by design: SQL injection, auth bypass,
server-side RCE, SSRF, and secret leakage are **not applicable** — there is no
server or data store to target.

## Hardening applied
- **HTTP security headers** via [`_headers`](./_headers) (Netlify): HSTS, CSP,
  X-Frame-Options: DENY, X-Content-Type-Options: nosniff, Referrer-Policy,
  Permissions-Policy, COOP/CORP.
- **Content Security Policy** restricting scripts/styles/fonts/images to a strict allowlist.
- **Clickjacking protection** (`frame-ancestors 'none'` + `X-Frame-Options: DENY`).
- **HTTPS enforced** (`upgrade-insecure-requests` + HSTS preload).
- **Outbound links** carry `rel="noopener noreferrer"` (no reverse-tabnabbing).
- **Booking form**: honeypot anti-bot field + client-side validation.
  (Server-side re-validation REQUIRED if a backend is added.)
- **Dependencies**: no runtime dependencies shipped to users. `npm audit` clean.

## If you connect a backend later (booking form)
1. Submit over **HTTPS only** to a trusted endpoint.
2. **Re-validate and sanitize every field server-side** — never trust the client.
3. Add **rate limiting / CAPTCHA** in addition to the honeypot.
4. Keep the API token in a server env var or the provider's form backend — **never in the HTML**.
5. Tighten the CSP `connect-src` / `form-action` to your exact endpoint.

## Reporting a vulnerability
Email **security@sparkleclean.com** (replace with your real address) with details.
Please allow a reasonable disclosure window before going public.
