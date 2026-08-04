# Parcels App (parcelsapp)

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

Parcels App (parcelsapp.com) is a universal parcel tracking service that tracks packages, air cargo (AWB), road freight (LTL/FTL), and sea freight across 1,540 postal operators, couriers, and logistics carriers worldwide - USPS, UPS, FedEx, DHL, Royal Mail, China Post, Cainiao, 4PX, and many more. The Parcels API v3 is an asynchronous shipment tracking API - create a tracking request, then poll by UUID or receive webhook callbacks until results are complete - with automatic carrier detection, localized tracking events, and cached results returned immediately.

**Access model:** The API is publicly documented (interactive reference plus a published OpenAPI 3.0.3 contract at `https://parcelsapp.com/api-docs/openapi.json`, including a keyless mock server for trying the flow). Live calls require an API key issued through the Parcels dashboard (`https://parcelsapp.com/dashboard/`), passed as an `apiKey` parameter, on a paid monthly subscription metered by unique tracking numbers per month ($19/$29/$49 published tiers). Parcels App offers a 30-day no-questions-asked refund on paid plans, and its API terms prohibit building a competing tracking website or app with it.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/parcelsapp/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/parcelsapp/refs/heads/main/apis.yml)

## Tags

- Parcel Tracking
- Shipment Status
- Package Tracking
- Logistics
- Shipping
- Carriers

## Timestamps

- **Created:** 2026-07-11
- **Modified:** 2026-07-11

## APIs

### Parcels App Shipments Tracking API

Asynchronous multi-carrier shipment tracking. `POST /shipments/tracking` creates a tracking request for one or more tracking numbers (with automatic carrier detection across 1,540 carriers), returning a UUID and any cached results immediately; `GET /shipments/tracking` polls by UUID until `done` is `true`. Optionally pass a `webhookUrl` to receive `shipment_completed` and `batch_completed` JSON callbacks instead of polling. Returns shipment status, origin/destination, detected carrier, and a full timeline of tracking events.

- **Human URL:** [https://parcelsapp.com/api-docs/](https://parcelsapp.com/api-docs/)
- **Base URL:** `https://parcelsapp.com/api/v3`

#### Tags

- Parcel Tracking
- Shipment Status
- Package Tracking
- Webhooks

#### Properties

- [Documentation](https://parcelsapp.com/api-docs/)
- [API Reference](https://parcelsapp.com/api-docs/openapi.json)
- [OpenAPI](openapi/parcelsapp-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/parcelsapp.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/parcelsapp.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Parcels App Account Usage API

`GET /account` returns the current subscription plan, monthly unique shipment limit, usage counter, and the UTC date the counter resets - letting integrations meter their tracking quota before creating new requests.

- **Human URL:** [https://parcelsapp.com/api-docs/](https://parcelsapp.com/api-docs/)
- **Base URL:** `https://parcelsapp.com/api/v3`

#### Tags

- Account
- Usage
- Quotas

#### Properties

- [Documentation](https://parcelsapp.com/api-docs/)
- [OpenAPI](openapi/parcelsapp-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/parcelsapp.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/parcelsapp.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

## Common Properties

- [Website](https://parcelsapp.com)
- [Documentation](https://parcelsapp.com/api-docs/)
- [Portal](https://parcelsapp.com/dashboard/)
- [Pricing](https://parcelsapp.com/pricing-api)
- [Terms Of Service](https://parcelsapp.com/terms-api)
- [Blog](https://parcelsapp.com/blog)
- [Plans](plans/parcelsapp-plans-pricing.yml)
- [Rate Limits](rate-limits/parcelsapp-rate-limits.yml)
- [Fin Ops](finops/parcelsapp-finops.yml)

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com
