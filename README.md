# United States Postal Service

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

The United States Postal Service (USPS) provides a modern REST API platform at developers.usps.com that gives ecommerce websites, shipping software, and logistics systems access to postal data and services. APIs cover address validation, package tracking, domestic and international shipping labels, pricing, carrier pickup scheduling, location finding, and Informed Delivery campaign management. The legacy Web Tools platform was retired January 25, 2026, with all functionality migrated to the new OAuth 2.0-secured API platform.

**Areas:** Government · Postal Service · Shipping · Logistics · Address Validation · Package Tracking

## United States Postal Service on APIs.io

Everything profiled for United States Postal Service is published on APIs.io rather than in this repository. Start at the provider page — **[apis.io/providers/usps/](https://apis.io/providers/usps/)** — or go straight to one of the APIs or properties below.

### APIs (12)

- [USPS International Prices API](https://apis.io/apis/usps/usps-international-prices-api/) — Provides pricing for international USPS products based on shipment characteristics including destination country, weight, dimensions, and service class.
- [USPS Domestic Labels API](https://apis.io/apis/usps/labels/) — Creates domestic shipping labels with barcodes in multiple formats and generates Shipping Services Files. Requires USPS Ship enrollment and Enterprise…
- [USPS International Labels API](https://apis.io/apis/usps/usps-international-labels-api/) — Creates international shipping labels and generates required Shipping Services Files for customs compliance.
- [USPS Locations API](https://apis.io/apis/usps/usps-locations-api/) — Identifies drop-off facilities and destination entry points for various USPS services. Supports post office locator and drop-off location finder.
- [USPS Service Standards API](https://apis.io/apis/usps/usps-service-standards-api/) — Provides delivery benchmarks showing expected transit times between origin and destination ZIP Codes for USPS mail classes.
- [USPS Shipping Options API](https://apis.io/apis/usps/usps-shipping-options-api/) — Returns a comprehensive list of pricing, service standards, and shipping options for USPS products in a single API call, eliminating the need to query…
- [USPS SCAN Forms API](https://apis.io/apis/usps/usps-scan-forms-api/) — Links multiple domestic and international labels through a single electronic file number, creating Shipment Confirmation Acceptance Notice forms for batch…
- [USPS OAuth API](https://apis.io/apis/usps/oauth2/) — Industry-standard OAuth 2.0 Client Credentials authentication protecting access to all USPS APIs. Returns Bearer Tokens used in the Authorization header for…
- [United States Postal Service Addresses API](https://apis.io/apis/usps/usps-addresses-api/) — Address validation and standardization operations
- [United States Postal Service Carrier Pickup API](https://apis.io/apis/usps/usps-carrier-pickup-api/) — Schedule and manage USPS carrier pickup requests
- [United States Postal Service Domestic Prices API](https://apis.io/apis/usps/usps-domestic-prices-api/) — Domestic postage pricing and rate calculation operations
- [United States Postal Service Tracking API](https://apis.io/apis/usps/usps-tracking-api/) — Package tracking status and event operations

### Published properties

Each property below is a page on APIs.io carrying the machine-readable artifact and what it says.

#### GraphQL (1)

GraphQL schemas.

- [Moved to /providers/usps/](https://apis.io/graphqls/usps/usps-graphql/)

#### Agentic access (1)

Which operations an agent can call, which act, and which need a human in the loop.

- [United States Postal Service Agentic Access](https://apis.io/agentic-access/usps/united-states-postal-service-agentic-access/)

#### JSON Schema (18)

The data models the API reads and writes.

- [Address](https://apis.io/schemas/usps/addresses-address/)
- [CityState](https://apis.io/schemas/usps/addresses-city-state/)
- [ZIPCodeResult](https://apis.io/schemas/usps/addresses-zip-code-result/)
- [PickupAddress](https://apis.io/schemas/usps/carrier-pickup-pickup-address/)
- [PickupPackage](https://apis.io/schemas/usps/carrier-pickup-pickup-package/)
- [PickupRequest](https://apis.io/schemas/usps/carrier-pickup-pickup-request/)
- [PickupResponse](https://apis.io/schemas/usps/carrier-pickup-pickup-response/)
- [PickupUpdateRequest](https://apis.io/schemas/usps/carrier-pickup-pickup-update-request/)
- [BaseRateRequest](https://apis.io/schemas/usps/domestic-prices-base-rate-request/)
- [ExtraServiceRateRequest](https://apis.io/schemas/usps/domestic-prices-extra-service-rate-request/)
- [ExtraServiceRateResponse](https://apis.io/schemas/usps/domestic-prices-extra-service-rate-response/)
- [RateResponse](https://apis.io/schemas/usps/domestic-prices-rate-response/)
- [TotalRateRequest](https://apis.io/schemas/usps/domestic-prices-total-rate-request/)
- [TotalRateResponse](https://apis.io/schemas/usps/domestic-prices-total-rate-response/)
- [MultipleTrackingRequest](https://apis.io/schemas/usps/tracking-multiple-tracking-request/)
- [MultipleTrackingResult](https://apis.io/schemas/usps/tracking-multiple-tracking-result/)
- [TrackingEvent](https://apis.io/schemas/usps/tracking-tracking-event/)
- [TrackingResult](https://apis.io/schemas/usps/tracking-tracking-result/)

#### JSON Structure (18)

Data models expressed in JSON Structure.

- [Addresses Address Structure](https://apis.io/json-structure/usps/addresses-address-structure/)
- [Addresses City State Structure](https://apis.io/json-structure/usps/addresses-city-state-structure/)
- [Addresses Zip Code Result Structure](https://apis.io/json-structure/usps/addresses-zip-code-result-structure/)
- [Carrier Pickup Pickup Address Structure](https://apis.io/json-structure/usps/carrier-pickup-pickup-address-structure/)
- [Carrier Pickup Pickup Package Structure](https://apis.io/json-structure/usps/carrier-pickup-pickup-package-structure/)
- [Carrier Pickup Pickup Request Structure](https://apis.io/json-structure/usps/carrier-pickup-pickup-request-structure/)
- [Carrier Pickup Pickup Response Structure](https://apis.io/json-structure/usps/carrier-pickup-pickup-response-structure/)
- [Carrier Pickup Pickup Update Request Structure](https://apis.io/json-structure/usps/carrier-pickup-pickup-update-request-structure/)
- [Domestic Prices Base Rate Request Structure](https://apis.io/json-structure/usps/domestic-prices-base-rate-request-structure/)
- [Domestic Prices Extra Service Rate Request Structure](https://apis.io/json-structure/usps/domestic-prices-extra-service-rate-request-structure/)
- [Domestic Prices Extra Service Rate Response Structure](https://apis.io/json-structure/usps/domestic-prices-extra-service-rate-response-structure/)
- [Domestic Prices Rate Response Structure](https://apis.io/json-structure/usps/domestic-prices-rate-response-structure/)
- [Domestic Prices Total Rate Request Structure](https://apis.io/json-structure/usps/domestic-prices-total-rate-request-structure/)
- [Domestic Prices Total Rate Response Structure](https://apis.io/json-structure/usps/domestic-prices-total-rate-response-structure/)
- [Tracking Multiple Tracking Request Structure](https://apis.io/json-structure/usps/tracking-multiple-tracking-request-structure/)
- [Tracking Multiple Tracking Result Structure](https://apis.io/json-structure/usps/tracking-multiple-tracking-result-structure/)
- [Tracking Tracking Event Structure](https://apis.io/json-structure/usps/tracking-tracking-event-structure/)
- [Tracking Tracking Result Structure](https://apis.io/json-structure/usps/tracking-tracking-result-structure/)

#### JSON-LD (4)

Linked-data contexts for the provider's vocabulary.

- [United States Postal Service Addresses Context](https://apis.io/jsonld/usps/united-states-postal-service-addresses-context/)
- [United States Postal Service Carrier Context](https://apis.io/jsonld/usps/united-states-postal-service-carrier-context/)
- [United States Postal Service Domestic Context](https://apis.io/jsonld/usps/united-states-postal-service-domestic-context/)
- [United States Postal Service Tracking Context](https://apis.io/jsonld/usps/united-states-postal-service-tracking-context/)

#### Examples (18)

Example requests and responses.

- [Addresses Address Example](https://apis.io/examples/usps/addresses-address-example/)
- [Addresses City State Example](https://apis.io/examples/usps/addresses-city-state-example/)
- [Addresses Zip Code Result Example](https://apis.io/examples/usps/addresses-zip-code-result-example/)
- [Carrier Pickup Pickup Address Example](https://apis.io/examples/usps/carrier-pickup-pickup-address-example/)
- [Carrier Pickup Pickup Package Example](https://apis.io/examples/usps/carrier-pickup-pickup-package-example/)
- [Carrier Pickup Pickup Request Example](https://apis.io/examples/usps/carrier-pickup-pickup-request-example/)
- [Carrier Pickup Pickup Response Example](https://apis.io/examples/usps/carrier-pickup-pickup-response-example/)
- [Carrier Pickup Pickup Update Request Example](https://apis.io/examples/usps/carrier-pickup-pickup-update-request-example/)
- [Domestic Prices Base Rate Request Example](https://apis.io/examples/usps/domestic-prices-base-rate-request-example/)
- [Domestic Prices Extra Service Rate Request Example](https://apis.io/examples/usps/domestic-prices-extra-service-rate-request-example/)
- [Domestic Prices Extra Service Rate Response Example](https://apis.io/examples/usps/domestic-prices-extra-service-rate-response-example/)
- [Domestic Prices Rate Response Example](https://apis.io/examples/usps/domestic-prices-rate-response-example/)
- [Domestic Prices Total Rate Request Example](https://apis.io/examples/usps/domestic-prices-total-rate-request-example/)
- [Domestic Prices Total Rate Response Example](https://apis.io/examples/usps/domestic-prices-total-rate-response-example/)
- [Tracking Multiple Tracking Request Example](https://apis.io/examples/usps/tracking-multiple-tracking-request-example/)
- [Tracking Multiple Tracking Result Example](https://apis.io/examples/usps/tracking-multiple-tracking-result-example/)
- [Tracking Tracking Event Example](https://apis.io/examples/usps/tracking-tracking-event-example/)
- [Tracking Tracking Result Example](https://apis.io/examples/usps/tracking-tracking-result-example/)

#### Collections (8)

Postman and Open Collection request collections.

- [USPS Addresses API](https://apis.io/collections/usps/open-united-states-postal-service-addresses/)
- [USPS Addresses API](https://apis.io/collections/usps/open-united-states-postal-service-addresses-api/)
- [USPS Carrier Pickup API](https://apis.io/collections/usps/open-united-states-postal-service-carrier-pickup/)
- [USPS Addresses Carrier Pickup API](https://apis.io/collections/usps/open-united-states-postal-service-carrier-pickup-api/)
- [USPS Domestic Prices API](https://apis.io/collections/usps/open-united-states-postal-service-domestic-prices/)
- [USPS Addresses Domestic Prices API](https://apis.io/collections/usps/open-united-states-postal-service-domestic-prices-api/)
- [USPS Tracking API](https://apis.io/collections/usps/open-united-states-postal-service-tracking/)
- [USPS Addresses Tracking API](https://apis.io/collections/usps/open-united-states-postal-service-tracking-api/)

#### Governance rules (2)

Spectral rulesets for the provider's contracts.

- [United States Postal Service — united states postal service jsonschema rules](https://apis.io/rules/usps/united-states-postal-service-jsonschema-spectral-rules/)
- [United States Postal Service — united states postal service rules](https://apis.io/rules/usps/united-states-postal-service-spectral-rules/)

#### Security (3)

Authentication, trust centre, and vulnerability disclosure.

- [United States Postal Service Authentication](https://apis.io/security/usps/united-states-postal-service-authentication/)
- [United States Postal Service Domain Security](https://apis.io/security/usps/united-states-postal-service-domain-security/)
- [Usps Domain Security](https://apis.io/security/usps/usps-domain-security/)

#### Plans and pricing (1)

Published plans, tiers and prices.

- [United States Postal Service Plans Pricing](https://apis.io/plans/usps/united-states-postal-service-plans-pricing/)

#### Rate limits (1)

Published request limits.

- [United States Postal Service Rate Limits](https://apis.io/rate-limits/usps/united-states-postal-service-rate-limits/)

#### FinOps (1)

What the API costs to run, by operation.

- [United States Postal Service Finops](https://apis.io/finops/usps/united-states-postal-service-finops/)

## Where to find this API

Links to the company's own pages. This repository publishes no copy of their specifications — the canonical document is theirs and lives at the URLs below.

- [Website](https://www.usps.com/)
- [Documentation](https://developers.usps.com/apis)
- [Getting started](https://developers.usps.com/getting-started)
- [Support](https://emailus.usps.com/s/web-tools-inquiry)
- [Blog](https://about.usps.com/news/latestnews.rss)
- [Terms of service](https://developers.usps.com/terms-and-conditions)
- [GitHub](https://github.com/USPS)

## API Evangelist rating

**Kin Score 33.8** — thin · rubric 0.24.0 · scored 2026-10-17

| Facet | Score |
|---|---|
| Discoverability | 71.4 |
| Contract quality | 33.7 |
| Contract governance | 27.3 |
| Operational transparency | 10.5 |
| Developer ergonomics | 50.0 |
| Access clarity | 15.8 |

**Agent readiness 30.4** — agent-ready

| Agent-readiness dimension | Result |
|---|---|
| Spec Presence | yes |
| Agentic Access | derived (partial credit) |
| Reversibility Documented | documented (partial credit) |
| MCP Server | — |
| Auth Clarity | bearer (partial credit) |
| Idempotency | — |
| Error Semantics | verified |
| OpenAPI Examples | verified |
| Rate Limit Signal | derived (partial credit) |
| Event Surface Described | — |
| Agent Skills | — |
| Well Known Catalog | — |
| Consent Identity | — |
| Agent Card | — |
| Dry Run Mode | — |
| Delegated Identity | — |
| Protected Resource Metadata | — |
| Dynamic Client Registration | — |
| Agentic Commerce | — |

**Regulatory alignment 20.6** — Government & Public Sector

The rubric is published at [github.com/api-evangelist/kin-score](https://github.com/api-evangelist/kin-score). The per-check breakdown behind these numbers — which checks were earned, partial or missed — along with score history and how this provider compares to its peers, is available at [apis.io/providers/usps/](https://apis.io/providers/usps/).

## How this profile is made

API Evangelist profiles a company's public API surface the way a developer would find it: the website, developer portal and documentation, the specifications it publishes, its public repositories, and its pricing, status and changelog pages. From that it derives the properties above — contracts split per API, workflows, schemas, collections, governance rules, plans and rate limits — and scores them against the published [Kin Score rubric](https://github.com/api-evangelist/kin-score).

The artifacts are published on [APIs.io](https://apis.io), not in this repository. This repository is the public record for United States Postal Service: the place to say something is wrong, missing or out of date, and to ask for a re-score or a removal.

## Open an issue

- **Something about this listing** — a wrong description, a missing API, a stale artifact or a question about the rating: [open an issue on this repository](https://github.com/api-evangelist/usps/issues/new).
- **A new API, or one that is not in the catalog yet** — [submit it on APIs.io](https://apis.io/add/).
- **Anything else** — [the APIs.io inbox](https://github.com/api-search/inbox/issues/new) or [info@apievangelist.com](mailto:info@apievangelist.com).
