# Ravelin (ravelin)

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
