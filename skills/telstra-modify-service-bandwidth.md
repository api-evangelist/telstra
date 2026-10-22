---
generated: '2026-10-20'
method: generated
name: modify-service-bandwidth
title: Modify service bandwidth or plan
description: List a customer's Telstra connectivity services, compare prices, submit a bandwidth or plan change, and poll
  the request status.
api: openapi/telstra-bandwidth-and-plan-modification-api-openapi.yml
operations:
- authToken
- listCustomerServices
- listPricing
- modifyBandwidth
- modifyAdaptivefibreBandwidth
- modifyAdaptiveBroadbandPlan
- fetchRequestStatus
source: Grounded in openapi/telstra-bandwidth-and-plan-modification-api-openapi.yml; operationIds verified verbatim in the
  spec.
---

# Modify service bandwidth or plan

List a customer's Telstra connectivity services, compare prices, submit a bandwidth or plan change, and poll the request status.

## Auth
OAuth2 client credentials: `authToken` (POST /token).

## Steps
1. `listCustomerServices` (GET /services) lists the customer's services (by CIDN).
2. `listPricing` (GET /services/price) shows the available tiers and prices.
3. Submit the change with the operation for the product: `modifyBandwidth` (Internet Direct), `modifyAdaptivefibreBandwidth` (Adaptive Fibre) or `modifyAdaptiveBroadbandPlan` (Adaptive Broadband).
4. Poll `fetchRequestStatus` (POST /requests/fetch-status, body requires `requestId`) until the request finishes.

## Rules
- A modify call changes a billed service. Confirm the target tier and price with the user, and never resubmit while a request is still pending.
