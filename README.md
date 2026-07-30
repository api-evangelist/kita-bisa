# Kita Bisa

Kitabisa is Indonesia's largest donation-based crowdfunding and mutual-aid platform,
founded in 2013 and headquartered in Jakarta. It serves individuals, nonprofits, and
corporations raising funds for medical causes, disaster relief, education, and community
development, and runs a dedicated Islamic-philanthropy surface for zakat, wakaf, and
qurban — alongside NGO fundraising services, a CSR practice, a cooperative, and the
SalingJaga mutual-protection product.

Website: https://kitabisa.com — Backed by: 500-global

## No public API

Kitabisa publishes **no public API and no developer program**. There is no developer
portal, API reference, or OpenAPI/AsyncAPI/GraphQL definition on any Kitabisa surface.
`docs.kitabisa.com` and `developer.kitabisa.com` do not resolve in DNS, and a code
search across all 75 public repositories in the `kitabisa` GitHub organization returns
zero OpenAPI or Swagger documents. Corporate and NGO integrations are arranged through
business partnership channels.

## What this repo captures

| Artifact | Path |
|---|---|
| Open source packages (Go, npm) | `packages/kita-bisa-packages.yml` |
| `/.well-known/` probe index | `well-known/kita-bisa-well-known.yml` |
| RFC 9116 security.txt (verbatim) | `well-known/kita-bisa-security.txt` |
| Vulnerability disclosure program | `security/kita-bisa-vulnerability-disclosure.yml` |
| Domain security posture | `security/kita-bisa-domain-security.yml` |
| llms.txt | `llms/kita-bisa-llms.txt` |

## Notable findings

- **Public responsible-disclosure program** at https://security.kitabisa.com, with the
  policy itself open-sourced at `github.com/kitabisa/responsible-disclosure`. Contact
  `infosec@kitabisa.com`; security.txt valid through 2027-12-30.
- **Strong domain posture**: TLS 1.3, DNSSEC enabled, CAA records set, SPF present,
  DMARC at `p=reject`. HSTS is not set.
- **Substantial open source estate**: 75 public repos including `teler-waf` (Go WAF
  middleware from the Kitabisa Security team), `sangu-dana` and `sangu-flip` (Go clients
  for Indonesian payment rails), and widely used GitHub Actions such as
  `sonarqube-action` and `docker-slim-action`.
- No SDK pointer is emitted: none of the published libraries are clients for a Kitabisa API.
