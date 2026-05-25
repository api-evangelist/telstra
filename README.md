# Telstra (telstra)
Telstra is Australia's largest telecommunications and mobile network operator, providing fixed broadband, mobile voice and data, enterprise networking, and IoT connectivity across Australia and into Asia. Telstra exposes a developer programme at dev.telstra.com fronting carrier-grade Messaging (SMS / MMS) and Mobile Number Verification APIs, with official SDKs in Python, Node.js, Java, .NET, and Go, and Arduino libraries for the Telstra Cat-1 and Cat-M1 IoT development kits. APIs are reached at `tapi.telstra.com` behind OAuth 2.0 client credentials with the `NSMS` or `MNV` scopes.

**URL:** [Visit APIs.json](https://raw.githubusercontent.com/api-evangelist/telstra/refs/heads/main/apis.yml)

**Run:** [Capabilities Using Naftiko](https://github.com/naftiko/fleet?utm_source=api-evangelist&utm_medium=readme&utm_campaign=company-api-evangelist&utm_content=repo)

## Tags

 - Telecommunications, Telco, Mobile, Messaging, SMS, MMS, Networks, Australia, Verification

## Timestamps

- **Created:** 2026-05-25
- **Modified:** 2026-05-25

## APIs

### Telstra Messaging API
Send and receive SMS and MMS messages programmatically across the Telstra mobile network. Outbound delivery to Australian and international destinations, inbound replies on provisioned dedicated virtual numbers, delivery status callbacks, scheduled delivery, and message validity windows. OAuth 2.0 client credentials with the `NSMS` scope.

**Base URL:** `https://tapi.telstra.com/v2`

**Human URL:** [https://dev.telstra.com](https://dev.telstra.com)

- [OpenAPI](openapi/telstra-messaging-api-openapi.yml)
- [JSON Schema — Message](json-schema/telstra-message-schema.json)
- [JSON Schema — Subscription](json-schema/telstra-subscription-schema.json)
- [JSON Structure — Message](json-structure/telstra-message-structure.json)
- [JSON-LD Context](json-ld/telstra-context.jsonld)
- [Example — Send SMS](examples/telstra-send-sms-example.json)
- [Example — OAuth Token](examples/telstra-oauth-token-example.json)
- [Example — Create Subscription](examples/telstra-create-subscription-example.json)
- [Naftiko Capability — SMS](capabilities/messaging-sms.yaml)
- [Naftiko Capability — MMS](capabilities/messaging-mms.yaml)
- [Naftiko Capability — Provisioning](capabilities/messaging-provisioning.yaml)
- [Naftiko Capability — Auth](capabilities/messaging-auth.yaml)

### Telstra Mobile Number Verification API
Silent, in-network verification of a Telstra mobile customer's MSISDN against the device's active mobile data session. Designed to replace SMS one-time-password flows. OAuth 2.0 client credentials with the `MNV` scope.

**Base URL:** `https://tapi.telstra.com/v1`

**Human URL:** [https://dev.telstra.com](https://dev.telstra.com)

- [OpenAPI](openapi/telstra-mobile-number-verification-api-openapi.yml)
- [Naftiko Capability — Mobile Number Verification](capabilities/mobile-number-verification.yaml)

## SDKs

| Language | Repository |
|---|---|
| Python | [telstra/MessagingAPI-SDK-python](https://github.com/telstra/MessagingAPI-SDK-python) |
| Node.js | [telstra/MessagingAPI-SDK-node](https://github.com/telstra/MessagingAPI-SDK-node) |
| Java | [telstra/MessagingAPI-SDK-Java](https://github.com/telstra/MessagingAPI-SDK-Java) |
| .NET | [telstra/MessagingAPI-SDK-dotnet](https://github.com/telstra/MessagingAPI-SDK-dotnet) |
| Go | [telstra/MessagingAPI-SDK-Go](https://github.com/telstra/MessagingAPI-SDK-Go) |

## IoT Tools

- [Cat-1-Development-Kit](https://github.com/telstra/Cat-1-Development-Kit) — Arduino library for the Telstra Cat-1 development kit.
- [Cat-M1-Dev-Board](https://github.com/telstra/Cat-M1-Dev-Board) — Arduino library for the Telstra Cat-M1 development board.

## Commercial Surface

- [Plans & Pricing](plans/telstra-plans-pricing.yml) — Free Trial tier and Paid (commercial) tier.
- [Rate Limits](rate-limits/telstra-rate-limits.yml) — Per-client_id throughput limits.
- [FinOps](finops/telstra-finops.yml) — Billing surfaces aligned with FOCUS.
- [Spectral Rules](rules/telstra-rules.yml) — Internal API conventions for Telstra specs.
- [Vocabulary](vocabulary/telstra-vocabulary.yml) — Concepts, services, tools, standards.

## Common Resources

- Developer Portal: [https://dev.telstra.com](https://dev.telstra.com)
- Corporate Site: [https://www.telstra.com.au](https://www.telstra.com.au)
- GitHub: [https://github.com/telstra](https://github.com/telstra)
- LinkedIn: [https://www.linkedin.com/company/telstra](https://www.linkedin.com/company/telstra)
- Telstra Exchange (blog): [https://exchange.telstra.com.au](https://exchange.telstra.com.au)
- CrowdSupport (forum): [https://crowdsupport.telstra.com.au](https://crowdsupport.telstra.com.au)
- Terms of Service: [https://www.telstra.com.au/business-enterprise/legal/messaging-api-terms-of-service](https://www.telstra.com.au/business-enterprise/legal/messaging-api-terms-of-service)
- Privacy: [https://www.telstra.com.au/privacy](https://www.telstra.com.au/privacy)

## Maintainers

| FN | Email | URL |
|---|---|---|
| Kin Lane | info@apievangelist.com | [apievangelist.com](https://apievangelist.com) |
