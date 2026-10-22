---
generated: '2026-10-20'
method: generated
name: check-sim-and-device-swap-risk
title: Check SIM and device swap risk
description: Fraud-check a mobile number before a sensitive action by asking whether its SIM or device was swapped recently
  (Telstra SIM Swap and Device Swap APIs).
api: openapi/telstra-sim-swap-api-openapi.yml
operations:
- authCode
- authToken
- checkSimSwap
- retrieveSimSwapDate
source: Grounded in openapi/telstra-sim-swap-api-openapi.yml; operationIds verified verbatim in the spec.
related_operations:
- api: openapi/telstra-device-swap-api-openapi.yml
  operations:
  - checkDeviceSwap
  - retrieveDeviceSwapDate
---

# Check SIM and device swap risk

Fraud-check a mobile number before a sensitive action by asking whether its SIM or device was swapped recently (Telstra SIM Swap and Device Swap APIs).

## Auth
OpenID Connect, the same way in both APIs: `authCode` (GET /auth), then `authToken` (POST /token). Each API is a separate contract with its own token endpoint (openapi/telstra-sim-swap-api-openapi.yml, openapi/telstra-device-swap-api-openapi.yml).

## Steps
1. Get a token for the SIM Swap API, then call `checkSimSwap` (POST /check) with `phoneNumber` and optional `maxAge` (look-back window) for a yes/no answer. Use `retrieveSimSwapDate` (POST /retrieve-date) when you need the timestamp.
2. Get a token for the Device Swap API, then call `checkDeviceSwap` (POST /check) or `retrieveDeviceSwapDate` (POST /retrieve-date) the same way.
3. If either check reports a recent swap, treat the action as higher risk (step-up auth or hold it).

## Rules
- These POSTs are read-only checks and safe to retry.
