# Security and Deployment

Security is a cross-cutting requirement from the first commit through production operations.

## V1 security posture

Prefer a static Astro build where possible. A static public site has no application server process handling every page request, reducing the runtime attack surface compared with an unnecessary server-rendered application.

Do not commit:

- `.env` secrets
- API keys/tokens
- private keys
- VPS credentials
- database credentials
- payment/provider secrets
- production-only configuration containing secrets

Public environment variables must be treated as public; never expose a secret to browser-delivered JavaScript.

## Contact form

The form architecture must be chosen before implementation. Review:

- server-side validation (when a server endpoint is used)
- spam/abuse protection
- rate limiting
- input length limits
- output encoding
- email/header injection risks if email delivery is involved
- CSRF where relevant to the chosen architecture
- privacy/data-retention implications
- useful, non-leaky error responses

Do not invent a backend merely to have a form; choose the smallest secure architecture that satisfies the requirement.

## Third-party content

External embeds can create privacy, tracking, CSP and performance implications. Prefer click-to-load/lazy loading for services such as video embeds. Keep third-party scripts to a minimum.

## Dependency hygiene

- keep Astro/Node dependencies current
- commit the package lockfile
- review dependency advisories
- remove unused packages
- avoid adding libraries for functionality that native browser APIs handle well

## VPS — discuss in detail before first production deployment

The exact setup depends on whether V1 remains fully static or later needs Node/server functionality. Do not install extra runtime software on the VPS until the deployment model is decided.

For a static Astro V1, the likely production model is:

1. Build the site to static output.
2. Serve the generated files through a hardened web server/reverse proxy such as Nginx or Caddy.
3. Use HTTPS with automatic certificate renewal.

Before launch, explicitly review and document:

- supported Linux distribution and patch/update policy
- non-root deployment/admin workflow
- SSH key authentication and root/password-login policy
- firewall rules and only required exposed ports
- web server configuration
- HTTPS/TLS and certificate renewal
- DNS
- file ownership and least-privilege permissions
- security headers, including a deliberate Content Security Policy
- HSTS only after HTTPS is confirmed correct
- MIME/content-type handling
- logs and log rotation
- backup/recovery strategy
- deployment method and rollback
- monitoring/availability needs
- brute-force protection where relevant
- secrets management if server-side functionality is introduced
- Node runtime/process manager only if server-side Astro/Node becomes necessary
- contact-form endpoint/service and its security controls

## Future account portal

An ASP.NET Core customer portal materially increases security responsibilities. Authentication, authorization, account recovery, sessions, customer data, entitlements, billing integrations, audit/logging and data protection must receive a dedicated threat/security design before implementation.

## Security review gates

Revisit security when:

- adding a form or server endpoint
- adding analytics or third-party scripts
- embedding external media
- accepting uploads
- adding downloads with access restrictions
- introducing commerce
- introducing authentication/accounts
- introducing APIs/databases
- changing VPS/deployment architecture
