# Ravelin (ravelin)

Ravelin is a London-based fraud detection and prevention platform offering AI-native, real-time decisioning APIs for online merchants. Their products cover payment fraud, chargeback recovery, account takeover (ATO) protection, refund and policy abuse, marketplace and supplier fraud, and a PSP-agnostic 3D Secure server. Ravelin combines per-merchant machine learning models, graph network analysis, and a consortium database of identity signals to score every customer interaction across checkout, login, registration, and post-transaction events.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/ravelin/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/ravelin/refs/heads/main/apis.yml)

## Scope

- **Type:** Index

## Tags

- Fraud Prevention
- Fraud Detection
- Chargeback Prevention
- Account Takeover
- 3D Secure
- Risk Scoring
- Payments
- Machine Learning

## Timestamps

- **Created:** 2026-05-25
- **Modified:** 2026-05-25

## APIs

### Ravelin Merchant API

The Ravelin Merchant API is a REST interface for submitting customer, order, transaction, payment, login, registration, voucher, supplier, dispute, refund, payout, and reclaim events to Ravelin and receiving back real-time risk decisions (ALLOW / REVIEW / PREVENT) with a 0-100 fraud score, the matched rules, and warnings. All endpoints are POST-only under https://api.ravelin.com, authenticated with a secret API key in the Authorization header, and respond with a structured decision envelope including action, source, score, scoreId, and any triggered rules.

- **Human URL:** [https://developer.ravelin.com/merchant/](https://developer.ravelin.com/merchant/)
- **Base URL:** `https://api.ravelin.com`

#### Tags

- Fraud Prevention
- Fraud Detection
- Chargeback Prevention
- Risk Scoring
- Account Takeover

#### Properties

- [Documentation](https://developer.ravelin.com/merchant/)
- [API Reference](https://developer.ravelin.com/merchant/api/)
- [Authentication](https://developer.ravelin.com/merchant/api/authentication/)
- [Rate Limits](https://developer.ravelin.com/merchant/api/rate-limits/)
- [Errors](https://developer.ravelin.com/merchant/api/errors/)
- [Warnings](https://developer.ravelin.com/merchant/api/warnings/)
- [Guarantees](https://developer.ravelin.com/merchant/api/guarantees/)
- [T L S](https://developer.ravelin.com/merchant/api/tls/)
- [Load Testing](https://developer.ravelin.com/merchant/api/load-testing/)
- [OpenAPI](openapi/ravelin-merchant-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/ravelin-merchant-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/ravelin-merchant-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Ravelin 3D Secure Server API

A PSP-agnostic, PCI 3DS-validated 3D Secure Server API for authenticating cardholders under EMV 3DS 2.x. Provides the Authentication Request (AReq), Challenge, Result, and Version Lookup operations against 3ds.live.pci.ravelin.com. Supports dynamic exemption routing, card scheme-specific fields (CAVV/AAV/AEVV), liability shift signaling, and integration with iOS, Android, and browser-side SDKs.

- **Human URL:** [https://developer.ravelin.com/merchant/api/endpoints/3d-secure/authenticate/](https://developer.ravelin.com/merchant/api/endpoints/3d-secure/authenticate/)
- **Base URL:** `https://3ds.live.pci.ravelin.com`

#### Tags

- 3D Secure
- EMV 3DS
- Strong Customer Authentication
- PSD2
- Payments

#### Properties

- [Documentation](https://developer.ravelin.com/merchant/api/endpoints/3d-secure/authenticate/)
- [API Reference](https://developer.ravelin.com/merchant/api/endpoints/3d-secure/)
- [Errors](https://developer.ravelin.com/merchant/api/endpoints/3d-secure/errors/)
- [Test Cards](https://developer.ravelin.com/merchant/api/endpoints/3d-secure/test-cards/)
- [Reference Implementation](https://github.com/unravelin/ravelin-3ds-demo)
- [OpenAPI](openapi/ravelin-3ds-server-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/ravelin-3ds-server-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/ravelin-3ds-server-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Ravelin PSP API

A purpose-built API surface for Payment Service Providers (PSPs) embedding Ravelin's risk scoring and dispute capture into their own merchant-facing product. Exposes Score, Transaction, Dispute, and the full 3D Secure operation set under the same authentication and decision envelope as the Merchant API.

- **Human URL:** [https://developer.ravelin.com/](https://developer.ravelin.com/)
- **Base URL:** `https://api.ravelin.com`

#### Tags

- Fraud Prevention
- Payment Service Provider
- Risk Scoring
- Disputes

#### Properties

- [Documentation](https://developer.ravelin.com/)
- [Authentication](https://developer.ravelin.com/merchant/api/authentication/)
- [Postman Collection](collections/ravelin-3ds-server-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/ravelin-3ds-server-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/ravelin-callbacks-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/ravelin-callbacks-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/ravelin-merchant-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/ravelin-merchant-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Ravelin Callbacks API

Outbound webhook callbacks delivered by Ravelin to merchant-configured endpoints when manual reviews, order decisions, or refund decisions are completed in the Ravelin dashboard. Used to keep order-management, fulfillment, and customer-service systems in sync with Ravelin's human-in-the-loop review outcomes.

- **Human URL:** [https://developer.ravelin.com/merchant/api/callbacks/order-decisions/](https://developer.ravelin.com/merchant/api/callbacks/order-decisions/)

#### Tags

- Webhooks
- Callbacks
- Manual Review
- Order Management

#### Properties

- [Documentation](https://developer.ravelin.com/merchant/api/callbacks/order-decisions/)
- [API Reference](https://developer.ravelin.com/merchant/api/callbacks/)
- [OpenAPI](openapi/ravelin-callbacks-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/ravelin-callbacks-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/ravelin-callbacks-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

## Common Properties

- [Website](https://www.ravelin.com/)
- [Portal](https://developer.ravelin.com/)
- [Documentation](https://developer.ravelin.com/merchant/)
- [Sign Up](https://www.ravelin.com/contact-us)
- [Login](https://dashboard.ravelin.com/)
- [Pricing](https://www.ravelin.com/contact-us)
- [Terms of Service](https://www.ravelin.com/legal/terms-of-service)
- [Privacy Policy](https://www.ravelin.com/legal/privacy-policy)
- [Support](https://support.ravelin.com/)
- [Help Center](https://support.ravelin.com/)
- [Blog](https://www.ravelin.com/blog)
- [Changelog](https://updates.ravelin.com/en)
- [Release Notes](https://updates.ravelin.com/en)
- [Careers](https://www.ravelin.com/careers)
- [Contact Us](https://www.ravelin.com/contact-us)
- [GitHub Organization](https://github.com/unravelin)
- [LinkedIn](https://www.linkedin.com/company/ravelin/)
- [Twitter](https://twitter.com/ravelinhq)
- [SDK](https://github.com/unravelin/ravelinjs)
- [SDK](https://github.com/unravelin/ravelin-ruby)
- [SDK](https://github.com/unravelin/ravelin-core-ios-xcframework-distribution)
- [SDK](https://github.com/unravelin/ravelin-encrypt-ios-xcframework-distribution)
- [SDK](https://github.com/unravelin/ravelin-3ds-sdk-ios-xcframework-distribution)
- [SDK](https://developer.ravelin.com/merchant/libraries-and-sdks/android/core-sdk/android/)
- [Reference Implementation](https://github.com/unravelin/ravelin-3ds-demo)
- [Compliance](https://www.ravelin.com/)
- [Compliance](https://www.ravelin.com/)
- [Compliance](https://www.ravelin.com/)
- [Features](undefined)
- [Use Cases](undefined)
- [Integrations](undefined)
- [Solutions](undefined)

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com
