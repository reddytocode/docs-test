---
title: Consumer Applications
description: Invite a consumer to apply for a loan via the Belle Sponsor API
---

## Consumer Application Invitation

`POST /api/v1/sponsor/consumers/`

Initiates a consumer loan invitation. Momnt sends the invitation via **SMS** or **Email**.

- Only **one** of these fields is required.
- Providing **both** will result in an error.

### Callback: Consumer Application Callback

After the consumer completes the Momnt loan application UI, Momnt POSTs the application outcome to your `sponsor_callback_url`.

**The callback fires twice:**
1. When the application is approved or canceled.
2. When the consumer accepts the loan documents.

**Requirements:**
- A successful POST to this endpoint must occur first.
- The consumer must complete the application in the Momnt UI.

**Callback authentication:** Basic Auth (username/password pre-shared between Momnt and the sponsor).

**Response:** Momnt expects HTTP `200` or `201` to acknowledge receipt. Any other status is logged as an error. The payload is logged for informational/historical purposes and may contain anything the external partner wishes.

---

## Merchant Consumer Applications List

`GET /api/v1/sponsor/merchants/{merchant_uuid}/consumers/` *(see API reference)*

Returns a list of consumer applications associated with a specific merchant.

---

## Consumer Information Details

`GET /api/v1/sponsor/consumers/{consumer_uuid}/` *(see API reference)*

Returns detailed information about a specific consumer.

---

## Consumer Payment Portal — Account Email Request

`POST /api/v1/sponsor/consumers/payment-portal/` *(see API reference)*

Sends the consumer a link to their payment portal account.
