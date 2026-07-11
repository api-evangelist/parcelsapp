# Parcels App (parcelsapp)

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
