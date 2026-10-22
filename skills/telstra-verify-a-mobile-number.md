---
generated: '2026-10-20'
method: generated
name: verify-a-mobile-number
title: Verify a mobile number (network-based)
description: Confirm that the device making a request is using the mobile number it claims, via Telstra Number Verification
  (OIDC authorization-code flow over the mobile network).
api: openapi/telstra-number-verification-api-openapi.yml
operations:
- authCode
- authToken
- phoneNumberVerify
source: Grounded in openapi/telstra-number-verification-api-openapi.yml; operationIds verified verbatim in the spec.
---

# Verify a mobile number (network-based)

Confirm that the device making a request is using the mobile number it claims, via Telstra Number Verification (OIDC authorization-code flow over the mobile network).

## Auth
OpenID Connect. `authCode` (GET /auth) must run from the end-user's device on the Telstra mobile network. `authToken` (POST /token) exchanges the code for an access token.

## Steps
1. Redirect the user's device to `authCode` to get an authorization code.
2. Exchange the code with `authToken`.
3. Call `phoneNumberVerify` (POST /verify) with either `phoneNumber` or `hashedPhoneNumber`. The response says whether it matches the number the network sees.

## Rules
- The token is bound to the device session it was obtained on. Do not reuse it for another number.
