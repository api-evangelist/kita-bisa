# Kita Bisa

<!-- API-EVANGELIST-PROVENANCE:BEGIN -->
> ### About this repository
>
> **This is not our API.** This repository is an independent, third-party profile of a company's
> **publicly available** API surface, maintained by [API Evangelist](https://apievangelist.com).
> API Evangelist does not operate, host, resell, or support this company's APIs, and is not
> affiliated with or endorsed by the company unless stated on the profile.
>
> **Where the information came from.** Everything here is assembled from material a member of the
> public can reach with a browser and no credentials — the company's own website, developer portal
> and documentation, the specifications it publishes for public use (OpenAPI, AsyncAPI, JSON Schema,
> `apis.json`, `llms.txt` and similar), its public repositories, and its public status, pricing and
> changelog pages. **Nothing here is obtained by breaching a system, defeating an access control, or
> using credentials of any kind.**
>
> **The rating is an independent assessment.** The Kin Score and Agent Readiness rating are
> independently calculated scores of a company's *public* API artifacts, produced by API Evangelist
> against a published rubric. They are not certifications, endorsements, security assessments, or
> audits, and they score published artifacts — not the quality, safety, or security of the software.
>
> **Corrections, re-scores, and removal are free.** No partnership, contract, or purchase is
> required, and you do not need to justify the request.
>
> - **Something wrong?** Open an issue on this repository, or email
>   [info@apievangelist.com](mailto:info@apievangelist.com).
> - **Published something new?** Ask for a re-score and we will re-run the rating.
> - **Want the listing taken down?** Say so and we will honor it. The profile is reduced to your
>   company name, a factual description, and a link to your own site, and the company is recorded as
>   **unrated** — never scored zero for having asked.
>
> **Response times.** Acknowledgement within **one business day**; removal or restriction within
> **two business days**; corrections and re-scores within **five business days**.
>
> **Not from the company, and here with a question?** You are welcome here — we would rather be the
> front line and point you the right way than have a good report go nowhere. What this repository
> can answer is narrow, though, so it is worth knowing who you are actually looking for:
>
> - **A question about how the API works, an account, billing, or a bug in the service** — that is
>   the company's own support, not us. We profile this API; we do not operate it and cannot see
>   your account.
> - **A bug in an open-source project we only catalog** — file it on that project's own repository.
>   This has happened with a real and correct bug report that reached us instead of the people who
>   could fix it, which helped nobody.
> - **Anything about this listing itself** — the description, the tags, the rating, a missing or
>   wrong artifact — is ours. Open an issue here.
> - **Not sure, or something general about API Evangelist or APIs.io** — open an issue on the
>   [APIs.io Inbox](https://github.com/api-search/inbox) and we will route it.
>
> **This repository contains no software, and we will never ask you to download anything.** There is
> no build, release, installer, or binary here — only text and machine-readable API descriptions, so
> there is nothing here that can be "corrupt" or need "repairing". Any issue, comment, or email
> claiming otherwise and offering a download link is not from us and is hostile. Do not follow the
> link; it is a lure. Report it to GitHub and, if you like, tell us at
> [info@apievangelist.com](mailto:info@apievangelist.com) so we can take it down.
>
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

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
