---
generated: '2026-10-20'
method: generated
name: send-an-sms-or-mms
title: Send an SMS or MMS
description: Provision a Telstra virtual number (or free-trial recipients), send an SMS/MMS from it with the Messaging API
  v3, then track delivery and replies.
api: openapi/telstra-messaging-api-openapi.yml
operations:
- authToken
- assignNumber
- getNumbers
- createTrialNumbers
- sendMessages
- getMessageById
- getMessages
- getRecipientOptouts
source: Grounded in openapi/telstra-messaging-api-openapi.yml; operationIds verified verbatim in the spec.
---

# Send an SMS or MMS

Provision a Telstra virtual number (or free-trial recipients), send an SMS/MMS from it with the Messaging API v3, then track delivery and replies.

## Auth
OAuth2 client credentials: `authToken` (POST /oauth/token) exchanges your client_id/secret for a bearer token; send it as `Authorization: Bearer <token>` on every call.

## Steps
1. `assignNumber` (POST /virtual-numbers) to get a virtual number to send from (body: optional `replyCallbackUrl`, `tags`). `getNumbers` lists numbers you already hold.
2. On a free trial, register up to the allowed recipients with `createTrialNumbers` (body requires `freeTrialNumbers`).
3. `sendMessages` (POST /messages). Required: `to`, `from`; add `messageContent` and/or `multimedia`, optional `scheduleSend`, `deliveryNotification`, `statusCallbackUrl`, `tags`.
4. Track the result with `getMessageById` (GET /messages/{messageId}) or list with `getMessages`; delivery status can also arrive at `statusCallbackUrl`.
5. Before re-sending to a number, check `getRecipientOptouts` (GET /virtual-numbers/{virtual-number}/optouts).

## Rules
- `sendMessages` is not idempotent: retrying a timed-out POST can send a duplicate. Check `getMessages` before you retry.
- `deleteMessageById` and `deleteNumber` are destructive. Do not call them without the user confirming.
