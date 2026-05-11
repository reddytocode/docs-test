---
title: Merchant Offer Codes
description: Create and manage promotional offer codes for a merchant
---

## List Offer Codes

`GET /api/v1/sponsor/merchants/{merchant_uuid}/offer-code/`

Returns all offer codes for a given merchant.

**Path Parameters:**

| Parameter | Type | Description |
|---|---|---|
| `merchant_uuid` | UUID | The external organization ID (`external_org_id`) of the merchant |

---

## Create Offer Code

`POST /api/v1/sponsor/merchants/{merchant_uuid}/offer-code/`

Creates a new offer code for a merchant.

Authentication information (username and password) is required. Sponsor ID is determined by the credentials used.

---

## Retrieve Offer Code

`GET /api/v1/sponsor/merchants/{merchant_uuid}/offer-code/{id}/`

Returns a single offer code by ID.

---

## Update Offer Code

`PATCH /api/v1/sponsor/merchants/{merchant_uuid}/offer-code/{id}/`

Implements **soft deletion** for offer codes via `is_deleted`.

**Behavior:**
- Sets `is_deleted: true` to mark the offer code as deleted.
- Returns a custom success message when `is_deleted` changes from `false` to `true`.
- **Restoration is not allowed** — attempting to change `is_deleted` from `true` to `false` returns HTTP 400.

| Status | Meaning |
|---|---|
| 200 | Soft delete successful |
| 400 | Invalid deletion state transition (attempted restoration) |
