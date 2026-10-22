---
generated: '2026-10-20'
method: generated
name: book-a-field-appointment
title: Book a field workforce appointment
description: 'For Telstra field-workforce partners: find available appointment slots, reserve one for a task, and reschedule
  or cancel it later.'
api: openapi/telstra-field-workforce-partners-api-openapi.yml
operations:
- TaskList-Retrieve
- Task-Retrieve
- Appointment-QueryAvailableSlots
- Appointment-Reserve
- Appointment-Retrieve
- Appointment-Reschedule
- Appointment-Cancel
source: Grounded in openapi/telstra-field-workforce-partners-api-openapi.yml; operationIds verified verbatim in the spec.
---

# Book a field workforce appointment

For Telstra field-workforce partners: find available appointment slots, reserve one for a task, and reschedule or cancel it later.

## Auth
OAuth2 client credentials (`bearerAuth`). Send the bearer token on every call.

## Steps
1. `TaskList-Retrieve` (GET /task-list), then `Task-Retrieve` (GET /task-detail) for the task you are scheduling.
2. `Appointment-QueryAvailableSlots` (POST /appointment/slot-enquiry). The body requires `data`, plus an optional `correlationId`.
3. `Appointment-Reserve` (POST /appointment/reservation) books a returned slot.
4. Confirm with `Appointment-Retrieve` (GET /appointment). Change it with `Appointment-Reschedule` (POST /appointment/reschedule), or cancel with `Appointment-Cancel` (DELETE /appointment).

## Rules
- Pass a `correlationId` so retries can be traced. Reservation is not idempotent, so check `Appointment-Retrieve` before you retry.
- Cancel is destructive. Confirm with the user first.
