# Telstra (telstra)

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
