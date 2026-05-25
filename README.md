# Ravelin (ravelin)

Ravelin is a London-based fraud detection and prevention platform offering AI-native, real-time decisioning APIs for online merchants. Their products cover payment fraud, chargeback recovery, account takeover (ATO) protection, refund and policy abuse, marketplace and supplier fraud, and a PSP-agnostic 3D Secure server. Ravelin combines per-merchant machine learning models, graph network analysis, and a consortium identity database to score every customer interaction across checkout, login, registration, voucher, and post-transaction events.

**URL:** [Visit APIs.json](https://raw.githubusercontent.com/api-evangelist/ravelin/refs/heads/main/apis.yml)

**Run:** [Capabilities Using Naftiko](https://github.com/naftiko/fleet?utm_source=api-evangelist&utm_medium=readme&utm_campaign=company-api-evangelist&utm_content=repo)

## Tags

- Fraud Prevention, Fraud Detection, Chargeback Prevention, Account Takeover, 3D Secure, Risk Scoring, Payments, Machine Learning

## Timestamps

- **Created:** 2026-05-25
- **Modified:** 2026-05-25

## APIs

### Ravelin Merchant API
The primary REST surface (`https://api.ravelin.com`) for submitting customer, order, login, registration, transaction, payment, voucher, supplier, dispute, refund, payout, and reclaim events to Ravelin. Every endpoint is POST-only, accepts a JSON payload, and returns a decision envelope with `action` (ALLOW / REVIEW / PREVENT), `source`, a 0-100 `score`, a `scoreId`, the triggered `rules`, and any data-quality `warnings`. Authentication is via `Authorization: token sk_live_...` (or `sk_test_...`).

**Human URL:** [https://developer.ravelin.com/merchant/](https://developer.ravelin.com/merchant/)

- [Documentation](https://developer.ravelin.com/merchant/)
- [API Reference](https://developer.ravelin.com/merchant/api/)
- [Authentication](https://developer.ravelin.com/merchant/api/authentication/)
- [Rate Limits](https://developer.ravelin.com/merchant/api/rate-limits/)
- [Errors](https://developer.ravelin.com/merchant/api/errors/)
- [Warnings](https://developer.ravelin.com/merchant/api/warnings/)
- [Guarantees](https://developer.ravelin.com/merchant/api/guarantees/)
- [Load Testing](https://developer.ravelin.com/merchant/api/load-testing/)
- [OpenAPI](openapi/ravelin-merchant-api-openapi.yml)

### Ravelin 3D Secure Server API
PCI 3DS-validated, PSP-agnostic EMV 3DS 2.x server (`https://3ds.live.pci.ravelin.com`) implementing the Version Lookup, Authentication Request (AReq), Challenge, and Result operations. Supports both encrypted payment-method payloads and unencrypted PAN, dynamic exemption routing, and card-scheme verification values (CAVV / AAV / AEVV). Pairs with native iOS, Android, and browser SDKs.

**Human URL:** [https://developer.ravelin.com/merchant/api/endpoints/3d-secure/authenticate/](https://developer.ravelin.com/merchant/api/endpoints/3d-secure/authenticate/)

- [Documentation](https://developer.ravelin.com/merchant/api/endpoints/3d-secure/authenticate/)
- [API Reference](https://developer.ravelin.com/merchant/api/endpoints/3d-secure/)
- [Errors](https://developer.ravelin.com/merchant/api/endpoints/3d-secure/errors/)
- [Test Cards](https://developer.ravelin.com/merchant/api/endpoints/3d-secure/test-cards/)
- [Reference Implementation](https://github.com/unravelin/ravelin-3ds-demo)
- [OpenAPI](openapi/ravelin-3ds-server-api-openapi.yml)

### Ravelin PSP API
A purpose-built surface for Payment Service Providers embedding Ravelin's Score, Transaction, Dispute, and 3DS operations into their own merchant-facing product. Same authentication and decision envelope as the Merchant API.

**Human URL:** [https://developer.ravelin.com/](https://developer.ravelin.com/)

- [Documentation](https://developer.ravelin.com/)
- [Authentication](https://developer.ravelin.com/merchant/api/authentication/)

### Ravelin Callbacks API
Outbound webhooks delivered by Ravelin to merchant-configured HTTPS endpoints when a manual review, order decision, or refund decision is completed in the Ravelin dashboard. Keeps order management, fulfillment, and customer-service systems in sync with Ravelin's human-in-the-loop review outcomes.

**Human URL:** [https://developer.ravelin.com/merchant/api/callbacks/order-decisions/](https://developer.ravelin.com/merchant/api/callbacks/order-decisions/)

- [Order Decisions](https://developer.ravelin.com/merchant/api/callbacks/order-decisions/)
- [Manual Reviews](https://developer.ravelin.com/merchant/api/callbacks/manual-reviews/)
- [Refund Decisions](https://developer.ravelin.com/merchant/api/callbacks/refund-decisions/)
- [OpenAPI](openapi/ravelin-callbacks-api-openapi.yml)

## Features

- **Per-Merchant Machine Learning** — Custom ML models trained per merchant, not a single global model.
- **Graph Network Analysis** — Link analysis across customers, devices, payment instruments, and addresses to surface hidden fraud rings.
- **Consortium Identity Database** — 9+ billion identity elements shared across merchants for cross-tenant signal enrichment.
- **Real-Time Decisioning** — ALLOW / REVIEW / PREVENT returned synchronously on every event.
- **PSP-Agnostic 3D Secure** — Works with any acquirer or PSP, with native iOS, Android, and browser SDKs.
- **Manual Review Workflow** — Dashboard for human review with webhook callbacks to the merchant's OMS.
- **Rules Engine** — Merchant-authored rules layered over ML scores; supports active and passive (shadow) modes.
- **Per-Customer Rate Limiting** — 50 events/minute/customer guardrail returning PREVENT with `source=RATE_LIMIT`.

## Use Cases

- Online payment fraud and chargeback prevention
- Account takeover (ATO) protection on login and credential events
- Refund and policy abuse detection
- Promo, voucher, and loyalty abuse prevention
- Marketplace and supplier fraud (drivers, couriers, sellers)
- 3D Secure / SCA optimization with dynamic exemption routing

## SDKs and Libraries

- [RavelinJS — Browser SDK](https://github.com/unravelin/ravelinjs)
- [Ravelin Ruby](https://github.com/unravelin/ravelin-ruby)
- [Ravelin iOS Core SDK (XCFramework)](https://github.com/unravelin/ravelin-core-ios-xcframework-distribution)
- [Ravelin iOS Encrypt SDK (XCFramework)](https://github.com/unravelin/ravelin-encrypt-ios-xcframework-distribution)
- [Ravelin iOS 3DS SDK (XCFramework)](https://github.com/unravelin/ravelin-3ds-sdk-ios-xcframework-distribution)
- [Ravelin Android — Core SDK](https://developer.ravelin.com/merchant/libraries-and-sdks/android/core-sdk/android/)
- [Ravelin Android — 3DS SDK](https://developer.ravelin.com/merchant/libraries-and-sdks/android/3ds-sdk/android/)
- [Ravelin 3DS Server Reference Integration (Go)](https://github.com/unravelin/ravelin-3ds-demo)

## Common Properties

- [Website](https://www.ravelin.com/)
- [Developer Portal](https://developer.ravelin.com/)
- [Documentation](https://developer.ravelin.com/merchant/)
- [Dashboard Login](https://dashboard.ravelin.com/)
- [Support / Help Center](https://support.ravelin.com/)
- [Blog](https://www.ravelin.com/blog)
- [Product Updates / Changelog](https://updates.ravelin.com/en)
- [Careers](https://www.ravelin.com/careers)
- [Contact Sales / Pricing](https://www.ravelin.com/contact-us)
- [GitHub Organization](https://github.com/unravelin)
- [LinkedIn](https://www.linkedin.com/company/ravelin/)
- [Twitter / X](https://twitter.com/ravelinhq)

## Compliance

- PCI-DSS certified
- PCI 3DS validated
- ISO 27001:2022 compliant
- Visa Global Registry of Service Providers member

## Artifacts

### OpenAPI

- [Ravelin Merchant API](openapi/ravelin-merchant-api-openapi.yml)
- [Ravelin 3D Secure Server API](openapi/ravelin-3ds-server-api-openapi.yml)
- [Ravelin Callbacks API](openapi/ravelin-callbacks-api-openapi.yml)

## Maintainers

**FN:** Kin Lane

**Email:** kin@apievangelist.com
