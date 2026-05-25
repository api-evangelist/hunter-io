# Hunter (hunter-io)
Hunter.io is an email-intelligence and outbound platform that finds, verifies, and enriches professional email addresses at scale. Its public APIs cover Domain Search, Email Finder, Email Verifier, Email Count, Discover (company prospecting), Person/Company/Combined Enrichment, Leads management, and Account/usage inspection. Credit-based metering, plan-tiered monthly allowances, and per-endpoint rate limits make it a reference example of a usage-based B2B data API.

**URL:** [Visit APIs.json](https://raw.githubusercontent.com/api-evangelist/hunter-io/refs/heads/main/apis.yml)

**Run:** [Capabilities Using Naftiko](https://github.com/naftiko/fleet?utm_source=api-evangelist&utm_medium=readme&utm_campaign=company-api-evangelist&utm_content=repo)

## Tags

- Email Finder, Email Verifier, Lead Generation, Outreach, Prospecting, Enrichment, Sales, Marketing

## Timestamps

- **Created:** 2026-05-25
- **Modified:** 2026-05-25

## Plans

| Plan | Monthly | Annual (per mo) | Credits / mo | Email Accounts | Sequence Recipients |
|---|---|---|---|---|---|
| Free | $0 | $0 | 50 | 1 | 500 |
| Starter | $49 | $34 | 2,000 | 3 | — |
| Growth | $149 | $104 | 10,000 | 10 | 5,000 |
| Scale | $299 | $209 | 25,000 | 20 | 15,000 |
| Enterprise | Custom | Custom | Custom | Custom | Custom |

Annual billing applies a 30% discount across all paid tiers.

## APIs

### Hunter Domain Search API
Return all emails Hunter has indexed for a domain or company name with the inferred email pattern, per-email confidence, department, seniority, and verification. Costs 1 credit per request.

**Human URL:** [https://hunter.io/api-documentation/v2#domain-search](https://hunter.io/api-documentation/v2#domain-search)

- [Documentation](https://hunter.io/api-documentation/v2#domain-search)
- [OpenAPI](openapi/hunter-domain-search-api-openapi.yml)
- [JSON Schema — Email](json-schema/hunter-email-schema.json)
- [JSON-LD Context](json-ld/hunter-io-context.jsonld)
- [Example](examples/hunter-domain-search-example.json)
- [Naftiko Capability](capabilities/domain-search.yaml)

### Hunter Email Finder API
Predict the most likely email for a named person at a company. Accepts first/last name, full name, or LinkedIn handle plus a domain or company name. Returns confidence, position, social handles, sources, and verification.

**Human URL:** [https://hunter.io/api-documentation/v2#email-finder](https://hunter.io/api-documentation/v2#email-finder)

- [OpenAPI](openapi/hunter-email-finder-api-openapi.yml)
- [Example](examples/hunter-email-finder-example.json)
- [Naftiko Capability](capabilities/email-finder.yaml)

### Hunter Email Verifier API
Verify deliverability via MX, SMTP, regex, disposable, webmail, accept-all, and block checks plus Hunter's database. Returns a normalized status and 0-100 score. Returns 202 while verification is in flight.

**Human URL:** [https://hunter.io/api-documentation/v2#email-verifier](https://hunter.io/api-documentation/v2#email-verifier)

- [OpenAPI](openapi/hunter-email-verifier-api-openapi.yml)
- [JSON Schema — Verification](json-schema/hunter-verification-schema.json)
- [Example](examples/hunter-email-verifier-example.json)
- [Naftiko Capability](capabilities/email-verifier.yaml)

### Hunter Email Count API
Free, unauthenticated. Counts emails Hunter has indexed for a domain or company, broken down by personal/generic, department, and seniority. Does not consume credits.

**Human URL:** [https://hunter.io/api-documentation/v2#email-count](https://hunter.io/api-documentation/v2#email-count)

- [OpenAPI](openapi/hunter-email-count-api-openapi.yml)
- [Naftiko Capability](capabilities/email-count.yaml)

### Hunter Discover API
Find target companies via natural-language query or structured filters across industry, headcount, location, technology, funding, and keywords. Premium filters require a paid plan.

**Human URL:** [https://hunter.io/api-documentation/v2#discover](https://hunter.io/api-documentation/v2#discover)

- [OpenAPI](openapi/hunter-discover-api-openapi.yml)
- [Naftiko Capability](capabilities/discover.yaml)

### Hunter Enrichment API
Person, company, and combined enrichment endpoints. Optional `clearbit_format=true` returns responses in Clearbit shape for drop-in migration.

**Human URL:** [https://hunter.io/api-documentation/v2#enrichment](https://hunter.io/api-documentation/v2#enrichment)

- [OpenAPI](openapi/hunter-enrichment-api-openapi.yml)
- [Naftiko Capability](capabilities/enrichment.yaml)

### Hunter Account API
Plan, reset date, team id, and used/available counters for searches, verifications, and credits.

**Human URL:** [https://hunter.io/api-documentation/v2#account](https://hunter.io/api-documentation/v2#account)

- [OpenAPI](openapi/hunter-account-api-openapi.yml)
- [Naftiko Capability](capabilities/account.yaml)

### Hunter Leads API
CRUD plus upsert and filtered list for leads. Powers Campaigns and integrates with Discover and Email Finder. Lead operations do not consume credits.

**Human URL:** [https://hunter.io/api-documentation/v2#leads](https://hunter.io/api-documentation/v2#leads)

- [OpenAPI](openapi/hunter-leads-api-openapi.yml)
- [JSON Schema — Lead](json-schema/hunter-lead-schema.json)
- [Naftiko Capability](capabilities/leads.yaml)

## Rate Limits

| Endpoint | Per second | Per minute |
|---|---|---|
| /v2/domain-search | 15 | 500 |
| /v2/email-finder | 15 | 500 |
| /v2/email-verifier | 10 | 300 |
| /v2/email-count | 15 | — |
| /v2/discover | 5 | 50 |
| /v2/people/find | 15 | 500 |
| /v2/companies/find | 15 | 500 |
| /v2/combined/find | 15 | 500 |

A `429` indicates the per-second/per-minute window was exceeded; quota exhaustion is also signaled via `429` once the monthly credit allowance is consumed.

## Common Resources

- [Portal](https://hunter.io)
- [Documentation](https://hunter.io/api-documentation)
- [Pricing](https://hunter.io/pricing)
- [GitHub Org](https://github.com/hunter-io)
- [Status Page](https://status.hunter.io)
- [Privacy](https://hunter.io/privacy)
- [Terms](https://hunter.io/terms)

## Reconciled Artifacts

- [Plans](plans/hunter-io-plans-pricing.yml) — API Commons Plans 0.1
- [Rate Limits](rate-limits/hunter-io-rate-limits.yml) — API Commons Rate Limits 0.1
- [FinOps](finops/hunter-io-finops.yml) — FOCUS-aligned
- [Vocabulary](vocabulary/hunter-io-vocabulary.yml)
- [Spectral Rules](rules/hunter-io-rules.yml)
- [JSON Structure](json-structure/hunter-io-structure.json)
- [JSON-LD Context](json-ld/hunter-io-context.jsonld)
