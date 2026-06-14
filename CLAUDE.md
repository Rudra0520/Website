# Project memory

## Git workflow
- After making code changes for this project, **commit and push them to GitHub automatically** without waiting to be asked.
- Use clear, descriptive commit messages summarizing what changed.
- End every commit message with:
  `Co-Authored-By: Claude Opus 4.8 <noreply@anthropic.com>`
- Remote: https://github.com/Rudra0520/Website.git (branch: main)

## Project
- SparkleClean — single-file static cleaning-service website (`index.html`), vanilla HTML/CSS/JS, no backend.
- Deployed on Netlify (`_headers` provides HTTP security headers; takes effect on deploy).
- Security hardening in place: CSP, HSTS, honeypot form, etc. See `SECURITY.md`.

## Security constraints
- Never commit secrets/API keys. `.gitignore` covers `.env`, `*.key`, `*.pem`, `node_modules/`, `.claude/`.
- Do not edit `.claude/settings.local.json` without explicit permission.
