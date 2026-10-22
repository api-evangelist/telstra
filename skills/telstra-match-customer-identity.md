---
generated: '2026-10-20'
method: generated
name: match-customer-identity
title: Match customer identity (KYC)
description: Check customer-supplied identity attributes against Telstra subscriber records with KYC Match, and check how
  long the subscriber has held the number with KYC Tenure (OIDC CIBA flow).
api: openapi/telstra-kyc-match-api-openapi.yml
operations:
- authReqId
- authToken
- KYC_Match
source: Grounded in openapi/telstra-kyc-match-api-openapi.yml; operationIds verified verbatim in the spec.
related_operations:
- api: openapi/telstra-kyc-tenure-api-openapi.yml
  operations:
  - checkTenure
---

# Match customer identity (KYC)

Check customer-supplied identity attributes against Telstra subscriber records with KYC Match, and check how long the subscriber has held the number with KYC Tenure (OIDC CIBA flow).

## Auth
OpenID Connect CIBA. `authReqId` (POST /ext/ciba/auth) starts a backchannel authorization request for the subscriber, and `authToken` (POST /token) returns the access token. KYC Tenure (openapi/telstra-kyc-tenure-api-openapi.yml) uses the same pattern with its own endpoints.

## Steps
1. Start CIBA with `authReqId`, then poll or exchange with `authToken`.
2. Call `KYC_Match` (POST /match) with `phoneNumber` plus the attributes to check (`idDocument`, `name`, `givenName`, `familyName`, `address`, ...). It returns a match result for each attribute.
3. If you also need the account's age, get a KYC Tenure token and call `checkTenure` (POST /check-tenure).

## Rules
- Send only the attributes the user consented to share.
