# Hunter.io GraphQL Schema

Conceptual GraphQL schema for the Hunter.io email intelligence and outbound platform, derived from the Hunter.io REST API (https://hunter.io/api-documentation/v2).

## Overview

Hunter.io provides email finding, verification, enrichment, and lead management capabilities through a credit-based REST API. This GraphQL schema models the full surface of those capabilities as a single coherent type system, covering all eight endpoint groups: Domain Search, Email Finder, Email Verifier, Email Count, Discover, Enrichment, Leads, Campaigns, and Account.

## Schema File

- `hunter-io-schema.graphql` — full GraphQL SDL with 55+ named types

## Type Summary

### Domain and Contact Types

| Type | Description |
|---|---|
| `Domain` | Core domain entity with organization metadata, social handles, technology stack, and geography |
| `DomainSearch` | Top-level Domain Search response wrapping result and pagination meta |
| `DomainSearchResult` | Domain search result including emails array, pattern, and organization details |
| `DomainContacts` | Flattened list of contacts for a domain with inferred email pattern |
| `ContactResult` | Single contact returned from a domain search with confidence and sources |
| `EmailCount` | Free unauthenticated count of indexed emails for a domain, broken down by type, department, and seniority |
| `EmailPattern` | Inferred format pattern for a domain (e.g., `{first}.{last}`) with regex and confidence |

### Email Types

| Type | Description |
|---|---|
| `Email` | Email address record as returned from domain search with type, confidence, and social fields |
| `EmailDetails` | Extended email record including full verification result and source list |
| `EmailType` | Enum: `PERSONAL` or `GENERIC` |
| `EmailConfidence` | Enum: `HIGH`, `MEDIUM`, `LOW` |
| `PersonEmail` | Email result from the Email Finder endpoint |
| `EmailFinder` | Full Email Finder response with score, person data, and verification |
| `PersonSearch` | Paginated results for a person search query |

### Verification Types

| Type | Description |
|---|---|
| `VerificationStatus` | Enum: `VALID`, `INVALID`, `ACCEPT_ALL`, `WEBMAIL`, `DISPOSABLE`, `UNKNOWN` |
| `VerificationResult` | Full SMTP/MX/regex/database verification result with boolean checks and score |
| `EmailVerification` | Top-level Email Verifier response wrapping result and deliverability |
| `Deliverable` | Simplified deliverability summary with status and score |
| `AcceptAll` | Catch-all domain flag |
| `Disposable` | Disposable domain flag |
| `Webmail` | Webmail provider flag |
| `Pattern` | Email format pattern match flag |

### Source and URL Types

| Type | Description |
|---|---|
| `Source` | Web source where an email was observed, with URI, domain, and timestamps |
| `SourceType` | Enum: `WEB`, `EMAIL`, `LINKEDIN`, `OTHER` |
| `URL` | Scalar representing a URL string |
| `LinkedInURL` | LinkedIn profile URL with raw and normalized forms |

### Person Data Types

| Type | Description |
|---|---|
| `FirstName` | Value object for a person's first name |
| `LastName` | Value object for a person's last name |
| `FullName` | Composed name object with first and last components |
| `Twitter` | Twitter handle and profile URL |
| `LinkedIn` | LinkedIn handle and profile URL |
| `Phone` | Phone number with type classification |
| `Seniority` | Enum: `JUNIOR`, `SENIOR`, `EXECUTIVE` |
| `Department` | Enum covering executive, IT, finance, sales, legal, support, HR, marketing, and more |
| `PositionInfo` | Job title, seniority, and department for a contact |

### Enrichment Types

| Type | Description |
|---|---|
| `EnrichmentLevel` | Enum: `BASIC`, `STANDARD`, `ENHANCED` |
| `PersonEnrichment` | Full person profile from the Enrichment API including name, role, social handles, and geography |
| `CompanyEnrichment` | Company profile from the Enrichment API including funding, headcount, technologies, and social presence |
| `CombinedEnrichment` | Combined person and company enrichment result in a single response |

### Format and Pattern Types

| Type | Description |
|---|---|
| `Format` | Email address format descriptor with pattern string and regex |
| `RegexPattern` | Compiled regex expression for an email format pattern |

### Discover Types

| Type | Description |
|---|---|
| `DiscoverResult` | Single company result from the Discover prospecting API |
| `DiscoverSearch` | Paginated Discover search response with query metadata |

### Bulk Task Types

| Type | Description |
|---|---|
| `BulkTask` | Async bulk task record for email verification or domain search |
| `BulkEmail` | Individual email entry within a bulk verification task |
| `BulkDomain` | Individual domain entry within a bulk domain search task |
| `BulkTaskStatus` | Enum: `PENDING`, `IN_PROGRESS`, `COMPLETED`, `FAILED` |
| `BulkEmailFinderInput` | Input type for bulk email finder tasks |

### Leads and Prospects Types

| Type | Description |
|---|---|
| `Lead` | Full lead record with contact data, verification status, sending status, list membership, and custom attributes |
| `EmailLead` | Lightweight lead summary with email and statuses |
| `ProspectEntry` | Individual entry in a prospects list |
| `ProspectsList` | Named list of prospects for organizing leads and campaigns |

### Campaign Types

| Type | Description |
|---|---|
| `Campaign` | Outbound email campaign with status, engagement metrics, and contact list |
| `CampaignContact` | Individual recipient in a campaign with open, click, reply, and bounce tracking |

### Account and Usage Types

| Type | Description |
|---|---|
| `AccountInfo` | Authenticated account details including plan, team, and per-meter usage |
| `APIKey` | API key record with creation date, last-used date, and permissions |
| `UsageStat` | Used/available counter pair for a metered resource |
| `RequestCredit` | Credit balance with used, available, and reset date |
| `PlanLimit` | Aggregated plan limits covering searches, verifications, credits, and rate limits |
| `RateLimit` | Per-endpoint rate limit descriptor with rps, rpm, rph bounds |

### Meta Types

| Type | Description |
|---|---|
| `SearchMeta` | Pagination and parameter metadata attached to list responses |

## Query Operations

| Query | Description |
|---|---|
| `domainSearch` | Search all emails indexed for a domain, with type/seniority/department filters |
| `emailFinder` | Find the most likely email for a named person at a company or domain |
| `emailVerifier` | Verify deliverability of a single email address |
| `emailCount` | Free unauthenticated count of emails for a domain |
| `discover` | Find companies matching structured or natural-language criteria |
| `personEnrichment` | Enrich an email or LinkedIn handle into a person profile |
| `companyEnrichment` | Enrich a domain into a company profile |
| `combinedEnrichment` | Combined person and company enrichment from an email |
| `leads` | Paginated, filtered list of leads in the account |
| `lead` | Single lead by ID |
| `prospectsLists` | All prospects lists in the account |
| `prospectsList` | Single prospects list by ID |
| `campaigns` | All campaigns in the account |
| `campaign` | Single campaign by ID |
| `account` | Authenticated account info including plan and usage |
| `bulkTask` | Single bulk task by ID |
| `bulkTasks` | All bulk tasks in the account |

## Mutation Operations

| Mutation | Description |
|---|---|
| `createLead` | Create a new lead with contact data and optional list assignment |
| `updateLead` | Update a lead's fields by ID |
| `deleteLead` | Delete a lead by ID |
| `createProspectsList` | Create a named prospects list |
| `updateProspectsList` | Rename a prospects list |
| `deleteProspectsList` | Delete a prospects list |
| `createBulkEmailVerificationTask` | Submit a list of emails for bulk verification |
| `createBulkDomainSearchTask` | Submit a list of domains for bulk domain search |
| `createBulkEmailFinderTask` | Submit a list of name/domain pairs for bulk email finding |

## Source

- API Documentation: https://hunter.io/api-documentation/v2
- Provider: Hunter.io
- Schema type: Conceptual (REST-to-GraphQL mapping)
- Generated: 2026-06-14
