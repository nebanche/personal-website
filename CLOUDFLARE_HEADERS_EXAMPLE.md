# Cloudflare Headers (example rules)

Add a Transform Rule or Ruleset to set these headers on HTML responses:

- Strict-Transport-Security: max-age=63072000; includeSubDomains; preload
- Content-Security-Policy: default-src 'self'; img-src 'self' data:; font-src 'self'; script-src 'self'; style-src 'self' 'unsafe-inline'
- Referrer-Policy: no-referrer-when-downgrade
- X-Content-Type-Options: nosniff
- Permissions-Policy: interest-cohort=()
