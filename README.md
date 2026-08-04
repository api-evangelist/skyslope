# SkySlope (skyslope)

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
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

SkySlope is a real estate transaction management and digital forms platform used by brokerages, teams, and agents across the U.S. and Canada to store, manage, and audit transaction documents for compliance, prepare and e-sign forms, and manage offers. SkySlope reports it serves over 900,000 real estate professionals and manages more than 3 million transactions annually.

SkySlope runs a partner-oriented public API program. Reference documentation is public, but obtaining OAuth client credentials is **partner/brokerage-gated** - you work with SkySlope to get access, and some endpoints are marked partner-only / coming soon in the published reference.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/skyslope/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/skyslope/refs/heads/main/apis.yml)

## Access Model

- **Partner / brokerage-gated.** The Partnership / Forms API and Offers API reference docs are publicly viewable (rendered with Redoc), but credentials are issued through a SkySlope partner/brokerage relationship, not via public self-service signup.
- **OAuth 2.0.** The Partnership / Forms API uses the authorization-code flow with PKCE (authorize/token at `accounts.skyslope.com`, scope `forms.files`). The Offers API uses the client-credentials flow (`POST /ext/token`). All requests are Bearer-authenticated over HTTPS.
- **BETA surface.** A broader Transaction Management API is referenced on `api.skyslope.com`; the host is live and returns `401` without a token, but a complete public reference was not reachable at review time, so its endpoints are intentionally not modeled here.

## Tags

- Real Estate
- Transaction Management
- Digital Forms
- E-Signature
- Compliance
- PropTech
- Documents

## Timestamps

- **Created:** 2026-07-04
- **Modified:** 2026-07-04

## APIs

### SkySlope Partnership (Forms) API

Create and manage SkySlope listing and transaction files and their documents, contacts, envelopes, forms, libraries, and templates; retrieve signed documents; and subscribe to a signed-documents webhook. OAuth 2.0 authorization-code flow with PKCE.

- **Human URL:** [https://forms.skyslope.com/partner/api/docs](https://forms.skyslope.com/partner/api/docs)
- **Base URL:** `https://forms.skyslope.com/partner/api`

#### Tags

- Files
- Documents
- Forms
- Contacts
- Envelopes

#### Properties

- [API Reference](https://forms.skyslope.com/partner/api/docs)
- [OpenAPI](openapi/skyslope-forms-partnership-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)

### SkySlope Offers API

Retrieve listings, offers, offer details, and counts/analytics of listings and offers from SkySlope Offers for a given agent or date range. OAuth 2.0 client-credentials flow.

- **Human URL:** [https://offers.skyslope.com/offers-api/reference](https://offers.skyslope.com/offers-api/reference)
- **Base URL:** `https://offers.skyslope.com/offers-api`

#### Tags

- Offers
- Listings
- Analytics
- Reporting

#### Properties

- [API Reference](https://offers.skyslope.com/offers-api/reference)
- [OpenAPI](openapi/skyslope-offers-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)

### SkySlope Transaction Management API (BETA)

SkySlope's broader enterprise Transaction Management API, positioned for brokerages to query, extract, and build on top of their SkySlope transaction data for reporting tools, dashboards, and enterprise applications. Host is live and requires authentication; a full public reference was not reachable at review time, so endpoints are not modeled here.

- **Human URL:** [https://skyslope.com/general/unlocking-the-power-of-your-data/](https://skyslope.com/general/unlocking-the-power-of-your-data/)
- **Base URL:** `https://api.skyslope.com/api`

#### Tags

- Transactions
- Reporting
- Enterprise
- Beta

#### Properties

- [Documentation](https://skyslope.com/general/unlocking-the-power-of-your-data/)

## Common Properties

- [Website](https://skyslope.com)
- [LinkedIn](https://www.linkedin.com/company/skyslope)
- [Documentation](https://forms.skyslope.com/partner/api/docs)
- [Documentation](https://skyslope.com/general/unlocking-the-power-of-your-data/)
- [Integrations](https://skyslope.com/integrations/)
- [Plans](plans/skyslope-plans-pricing.yml)
- [Rate Limits](rate-limits/skyslope-rate-limits.yml)
- [Fin Ops](finops/skyslope-finops.yml)

## Pricing

SkySlope does not publicly list exact prices; plans are quote-based and vary by brokerage size, transaction volume, and add-ons. Third-party sources describe tiered plans (Essentials, Professional, Enterprise) with reported per-user rates in the low-tens up to roughly $60/user/month, and the SkySlope Suite reported starting around $340/month for brokerages. See [plans/skyslope-plans-pricing.yml](plans/skyslope-plans-pricing.yml). All figures are third-party estimates - verify with SkySlope sales.

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com
