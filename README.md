# Telstra (telstra)

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

Telstra is Australia's largest telecommunications and mobile network operator, providing fixed broadband, mobile voice and data, enterprise networking, and IoT connectivity across Australia and into Asia. Telstra exposes a developer programme at dev.telstra.com fronting carrier-grade Messaging (SMS / MMS) and Mobile Number Verification APIs, with official SDKs in Python, Node.js, Java, .NET, and Go, and Arduino libraries for the Telstra Cat-1 and Cat-M1 IoT development kits. APIs are reached at tapi.telstra.com behind OAuth 2.0 client credentials with the NSMS or MNV scopes.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/telstra/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/telstra/refs/heads/main/apis.yml)

## Scope

- **Position:** Consuming
- **Access:** 3rd-Party

## Tags

- Telecommunications
- Telco
- Mobile
- Messaging
- SMS
- MMS
- Networks
- Australia
- Verification

## Timestamps

- **Created:** 2026-05-25T00:00:00.000Z
- **Modified:** 2026-05-25

## APIs

### Telstra Messaging API

Send and receive SMS and MMS messages programmatically across the Telstra mobile network. Supports outbound delivery to Australian and international destinations, inbound replies on provisioned dedicated virtual numbers, delivery status callbacks, scheduled delivery, and message validity windows. Authentication uses OAuth 2.0 client credentials with the NSMS scope against /oauth/token.

- **Human URL:** [https://dev.telstra.com](https://dev.telstra.com)
- **Base URL:** `https://tapi.telstra.com/v2`

#### Tags

- Messaging
- SMS
- MMS
- Telecommunications
- Mobile

#### Properties

- [Documentation](https://dev.telstra.com)
- [OpenAPI](openapi/telstra-messaging-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/telstra-messaging-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/telstra-messaging-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [JSON Schema](json-schema/telstra-message-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON Schema](json-schema/telstra-subscription-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON Structure](json-structure/telstra-message-structure.json)
- [JSON-LD](json-ld/telstra-context.jsonld) — [JSON-LD](https://www.w3.org/TR/json-ld11/)
- [Example](examples/telstra-send-sms-example.json)
- [Example](examples/telstra-create-subscription-example.json)
- [SDK](https://github.com/telstra/MessagingAPI-SDK-python)
- [SDK](https://github.com/telstra/MessagingAPI-SDK-node)
- [SDK](https://github.com/telstra/MessagingAPI-SDK-Java)
- [SDK](https://github.com/telstra/MessagingAPI-SDK-dotnet)
- [SDK](https://github.com/telstra/MessagingAPI-SDK-Go)

### Telstra Mobile Number Verification API

Silent, in-network verification of a Telstra mobile customer's MSISDN against the device's active mobile data session. Designed to replace SMS one-time-password flows for sign-in, account recovery, and fraud-check workflows on the Telstra consumer network. Authentication uses OAuth 2.0 client credentials with the MNV scope.

- **Human URL:** [https://dev.telstra.com](https://dev.telstra.com)
- **Base URL:** `https://tapi.telstra.com/v1`

#### Tags

- Verification
- Identity
- Authentication
- Mobile
- Telecommunications

#### Properties

- [Documentation](https://dev.telstra.com)
- [OpenAPI](openapi/telstra-mobile-number-verification-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/telstra-mobile-number-verification-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/telstra-mobile-number-verification-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

## Common Properties

- [Portal](https://dev.telstra.com)
- [Portal](https://www.telstra.com.au)
- [Documentation](https://dev.telstra.com)
- [Sign Up](https://dev.telstra.com)
- [GitHub Organization](https://github.com/telstra)
- [Status Page](https://crowdsupport.telstra.com.au/t5/network-coverage/ct-p/Networkcoverage)
- [Terms of Service](https://www.telstra.com.au/business-enterprise/legal/messaging-api-terms-of-service)
- [Privacy Policy](https://www.telstra.com.au/privacy)
- [LinkedIn](https://www.linkedin.com/company/telstra)
- [Blog](https://exchange.telstra.com.au)
- [Support](https://www.telstra.com.au/support)
- [Forum](https://crowdsupport.telstra.com.au)
- [Git Hub](https://github.com/telstra)
- [SDK](https://github.com/telstra/MessagingAPI-SDK-python)
- [SDK](https://github.com/telstra/MessagingAPI-SDK-node)
- [SDK](https://github.com/telstra/MessagingAPI-SDK-Java)
- [SDK](https://github.com/telstra/MessagingAPI-SDK-dotnet)
- [SDK](https://github.com/telstra/MessagingAPI-SDK-Go)
- [License](https://github.com/telstra/tdev-doc-license)
- [Tool](https://github.com/telstra/Cat-1-Development-Kit)
- [Tool](https://github.com/telstra/Cat-M1-Dev-Board)
- [Plans](plans/telstra-plans-pricing.yml)
- [Rate Limits](rate-limits/telstra-rate-limits.yml)
- [Fin Ops](finops/telstra-finops.yml)
- [Spectral Ruleset](rules/telstra-rules.yml)
- [Vocabulary](vocabulary/telstra-vocabulary.yml)
- [Features](undefined)

## Maintainers

**FN:** Kin Lane
**Email:** info@apievangelist.com
**URL:** https://apievangelist.com
