---
title: Merchant Statements
description: Retrieve billing statements for a merchant
---

## List Statements

`GET /api/v1/sponsor/merchants/{request_user_id}/statement/`

Returns a list of billing statements for a merchant.

---

## Get Statement Detail

`GET /api/v1/sponsor/merchants/{request_user_id}/statement/{id}/`

Returns a single billing statement by ID.

**Path Parameters:**

| Parameter | Type | Description |
|---|---|---|
| `request_user_id` | string | The user ID of the merchant admin making the request |
| `id` | integer | The ID of the statement |
