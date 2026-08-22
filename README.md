# Hunter (hunter-io)

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

Hunter.io is an email-intelligence and outbound platform that finds, verifies, and enriches professional email addresses at scale. Its public APIs cover Domain Search, Email Finder, Email Verifier, Email Count, Discover (company prospecting), Person/Company/Combined Enrichment, Leads management, and Account/usage inspection. Credit-based metering, plan-tiered monthly allowances, and per-endpoint rate limits make it a reference example of a usage-based B2B data API.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/hunter-io/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/hunter-io/refs/heads/main/apis.yml)

## Scope

- **Position:** Consuming
- **Access:** 3rd-Party

## Tags

- Email Finder
- Email Verifier
- Lead Generation
- Outreach
- Prospecting
- Enrichment
- Sales
- Marketing

## Timestamps

- **Created:** 2026-05-25T00:00:00.000Z
- **Modified:** 2026-05-25

## APIs

### Hunter Domain Search API

Search for all email addresses associated with a domain name or company. Returns the inferred email pattern, organization metadata, and a list of emails with confidence scores, departments, seniority, verification status, and observed sources. Costs 1 credit per request.

- **Human URL:** [https://hunter.io/api-documentation/v2#domain-search](https://hunter.io/api-documentation/v2#domain-search)

#### Tags

- Email Finder
- Lead Generation
- Domain Search

#### Properties

- [Documentation](https://hunter.io/api-documentation/v2#domain-search)
- [OpenAPI](openapi/hunter-domain-search-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/hunter-domain-search-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/hunter-domain-search-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [JSON Schema](json-schema/hunter-email-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON-LD](json-ld/hunter-io-context.jsonld) — [JSON-LD](https://www.w3.org/TR/json-ld11/)
- [Examples](examples/hunter-domain-search-example.json)

### Hunter Email Finder API

Generate or retrieve the most likely email address for a named person at a company. Accepts first/last name, full name, or LinkedIn handle alongside a domain or company. Returns confidence score, position, social handles, sources, and verification status. Costs 1 credit per request.

- **Human URL:** [https://hunter.io/api-documentation/v2#email-finder](https://hunter.io/api-documentation/v2#email-finder)

#### Tags

- Email Finder
- Lead Generation

#### Properties

- [Documentation](https://hunter.io/api-documentation/v2#email-finder)
- [OpenAPI](openapi/hunter-email-finder-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/hunter-email-finder-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/hunter-email-finder-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [JSON Schema](json-schema/hunter-email-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [Examples](examples/hunter-email-finder-example.json)

### Hunter Email Verifier API

Verify the deliverability of an email address through MX-record inspection, SMTP connection checks, catch-all detection, disposable-domain detection, webmail detection, and Hunter's own database lookup. Returns a normalized status (valid, invalid, accept_all, webmail, disposable, unknown) plus a 0-100 confidence score. May return 202 while verification is in flight.

- **Human URL:** [https://hunter.io/api-documentation/v2#email-verifier](https://hunter.io/api-documentation/v2#email-verifier)

#### Tags

- Email Verifier
- Deliverability

#### Properties

- [Documentation](https://hunter.io/api-documentation/v2#email-verifier)
- [OpenAPI](openapi/hunter-email-verifier-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/hunter-email-verifier-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/hunter-email-verifier-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [JSON Schema](json-schema/hunter-verification-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [Examples](examples/hunter-email-verifier-example.json)

### Hunter Email Count API

Free, unauthenticated endpoint returning the total number of email addresses Hunter has indexed for a domain or company, broken down by personal/generic, department, and seniority. Does not consume credits.

- **Human URL:** [https://hunter.io/api-documentation/v2#email-count](https://hunter.io/api-documentation/v2#email-count)

#### Tags

- Email Finder
- Counts

#### Properties

- [Documentation](https://hunter.io/api-documentation/v2#email-count)
- [OpenAPI](openapi/hunter-email-count-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/hunter-email-count-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/hunter-email-count-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Hunter Discover API

Find companies matching a target customer profile using a natural-language query or structured filters across industry, headcount, location, technology stack, funding, and keywords. Powers Hunter's prospecting workflows and feeds Domain Search and Email Finder. Premium filters (similar_to, technology, funding, year_founded) require a higher plan.

- **Human URL:** [https://hunter.io/api-documentation/v2#discover](https://hunter.io/api-documentation/v2#discover)

#### Tags

- Discover
- Prospecting
- Lead Generation

#### Properties

- [Documentation](https://hunter.io/api-documentation/v2#discover)
- [OpenAPI](openapi/hunter-discover-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/hunter-discover-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/hunter-discover-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Hunter Enrichment API

Person, company, and combined enrichment. Turn an email or LinkedIn handle into a rich person profile (name, role, seniority, social handles, geo), turn a domain into a company profile (industry, location, technology stack, funding, metrics), or combine both in a single call. Supports a `clearbit_format=true` flag for drop-in Clearbit migration.

- **Human URL:** [https://hunter.io/api-documentation/v2#enrichment](https://hunter.io/api-documentation/v2#enrichment)

#### Tags

- Enrichment
- Person
- Company

#### Properties

- [Documentation](https://hunter.io/api-documentation/v2#enrichment)
- [OpenAPI](openapi/hunter-enrichment-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/hunter-enrichment-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/hunter-enrichment-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Hunter Account API

Returns information about the authenticated Hunter account, including plan name and level, credit reset date, team id, and per-meter usage counters (searches, verifications, credits) with used/available splits. Useful for FinOps and pre-flight quota checks.

- **Human URL:** [https://hunter.io/api-documentation/v2#account](https://hunter.io/api-documentation/v2#account)

#### Tags

- Account
- Usage
- FinOps

#### Properties

- [Documentation](https://hunter.io/api-documentation/v2#account)
- [OpenAPI](openapi/hunter-account-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/hunter-account-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/hunter-account-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Hunter Leads API

Manage leads saved in your Hunter account. Full CRUD plus upsert and filtered list, with pagination, query search, leads-list scoping, verification and sending-status filters, and custom attributes. Leads power Hunter's Campaigns surface and integrate with Hunter Discover and Email Finder. Lead operations do not consume credits.

- **Human URL:** [https://hunter.io/api-documentation/v2#leads](https://hunter.io/api-documentation/v2#leads)

#### Tags

- Leads
- CRM
- Campaigns

#### Properties

- [Documentation](https://hunter.io/api-documentation/v2#leads)
- [OpenAPI](openapi/hunter-leads-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/hunter-leads-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/hunter-leads-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [JSON Schema](json-schema/hunter-lead-schema.json) — [JSON Schema](https://json-schema.org/specification)

## Common Properties

- [Arazzo Workflows](arazzo/) — [Arazzo Specification](https://spec.openapis.org/arazzo/latest.html)
- [Portal](https://hunter.io)
- [Documentation](https://hunter.io/api-documentation)
- [Documentation](https://hunter.io/api-documentation/v2)
- [Getting Started](https://hunter.io/api-documentation/v2#introduction)
- [Authentication](https://hunter.io/api-documentation/v2#authentication)
- [Rate Limits](https://hunter.io/api-documentation/v2#rate-limiting)
- [Errors](https://hunter.io/api-documentation/v2#errors)
- [Changelog](https://hunter.io/api-documentation/v2#changelog)
- [Blog](https://hunter.io/blog)
- [Sign Up](https://hunter.io/users/sign_up)
- [Privacy Policy](https://hunter.io/privacy)
- [Terms of Service](https://hunter.io/terms)
- [Status Page](https://status.hunter.io)
- [Support](https://hunter.io/contact)
- [GitHub Organization](https://github.com/hunter-io)
- [Plugin](https://chrome.google.com/webstore/detail/hunter-find-email-address/hgmhmanijnjhaffoampdlllchpolkdnj)
- [Plugin](https://addons.mozilla.org/en-US/firefox/addon/hunterio/)
- [Integration](https://hunter.io/integrations/salesforce)
- [Integration](https://hunter.io/integrations/hubspot)
- [Integration](https://hunter.io/integrations/zapier)
- [Integration](https://hunter.io/integrations/pipedrive)
- [Integration](https://hunter.io/integrations/zoho)
- [Tool](https://hunter.io/email-pattern)
- [Tool](https://hunter.io/email-verifier)
- [Tool](https://hunter.io/email-finder)
- [Tool](https://hunter.io/bulks)
- [Tool](https://hunter.io/companies)
- [Resource](https://hunter.io/templates)
- [Glossary](https://hunter.io/email-marketing-glossary)
- [Plugin](https://github.com/hunter-io/claude-plugin)
- [Tool](https://github.com/hunter-io/chatgpt-mcp)
- [Tool](https://github.com/hunter-io/hunter-mcp)
- [Tool](https://github.com/hunter-io/mcp-oauth-proxy)
- [Tool](https://github.com/hunter-io/baseimage-ruby)
- [SDK](https://github.com/hunter-io/sentry-ruby)
- [Plans](plans/hunter-io-plans-pricing.yml)
- [Rate Limits](rate-limits/hunter-io-rate-limits.yml)
- [Fin Ops](finops/hunter-io-finops.yml)
- [Vocabulary](vocabulary/hunter-io-vocabulary.yml)
- [Spectral Rules](rules/hunter-io-rules.yml)
- [JSON Structure](json-structure/hunter-io-structure.json)
- [Features](undefined)

## Maintainers

**FN:** Kin Lane
**Email:** info@apievangelist.com
**URL:** https://apievangelist.com
