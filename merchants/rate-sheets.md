---
title: Merchant Rate Sheets
description: View and configure the loan products available to a merchant
---

## Overview

A rate sheet defines the loan products available to a merchant. Consumers who apply through a merchant with no selected products will not receive any offers. The rate sheet includes product descriptions, APRs, terms, and merchant fees.

An approved and active merchant should always have a rate sheet configured.

---

## Get Rate Sheet

`GET /api/v1/sponsor/merchants/rate-sheets/{request_user_id}/`

Returns the rate sheet for a given merchant.

**Requirements:**
- `request_user_id` must exist in the Momnt system, be active, and have Admin permission on this merchant/sponsor.
- This user should have been established during pre-onboarding or user creation.

**Query Parameters:**

| Parameter | Type | Description |
|---|---|---|
| `is_merchant_selected` | boolean | Filter by whether the product is selected by the merchant |

---

## Update Rate Sheet

`PATCH /api/v1/sponsor/merchants/rate-sheets/`

Update which loan products are selected on a merchant's rate sheet.
