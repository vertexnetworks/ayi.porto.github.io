# Faiq Faiqoh Yasmin — Creative Portfolio

Self-contained static portfolio deployed with GitHub Pages.

## Deployment

Pushes to `main` run the official GitHub Pages workflow in `.github/workflows/static.yml`.

Expected project-site URL:

- https://vertexnetworks.github.io/ayi.porto.github.io/

## Security and privacy

- No runtime dependencies or third-party scripts.
- Images and fonts are embedded as data URLs.
- A restrictive CSP blocks network connections, objects, frames, workers, and form submission.
- Referrer information is not sent during outbound navigation.
- GitHub Pages is public; the portfolio intentionally publishes the contact information present in `index.html`.

## OWASP static-site review

- Injection: pass — no server, form submission, template input, `eval`, or dynamic code execution.
- Broken authentication: not applicable — the portfolio has no authenticated area.
- Sensitive-data exposure: reviewed — public contact details are intentional; no credentials detected.
- XML external entities: not applicable — no XML processing.
- Broken access control: not applicable — all deployed content is public by design.
- Security misconfiguration: pass with platform limitation — restrictive meta CSP and referrer policy; transport headers are controlled by GitHub Pages.
- Cross-site scripting: pass — no untrusted input; lightbox content is assigned with `textContent`.
- Insecure deserialization: not applicable — no serialized input.
- Vulnerable components: pass — no runtime dependencies; deployment actions are SHA-pinned.
- Logging and monitoring: platform-provided — deployment history is retained in GitHub Actions; the static page has no application logs.
