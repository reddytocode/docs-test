---
title: Merchant Onboarding
description: Initiate merchant pre-onboarding via the Belle Sponsor API
---

## Merchant Pre-Onboarding

`POST /api/v1/sponsor/merchants/onboarding/`

The merchant's first step is requesting an invitation to apply. The sponsor submits the merchant's business and contact information to Momnt, which creates the initial account and sends the merchant an email invitation to complete their application.

The response includes Momnt's merchant-specific identifiers — store these for use in future API calls.

> **Address validation:** Momnt uses [Smarty Streets](https://smarty.com) for address verification. Ensure submitted addresses are valid and mailable.

### Notes for Testing

- Each successful POST creates a merchant account and the first merchant admin user.
- To test again, change `users_business_email`, `user_id`, and `contractor_id` to unique values per request.

### Error Responses

| Status | Message |
|---|---|
| 400 | `User Already Exists` |
| 400 | `Merchant Already Exists` |
| 400 | `Merchant User Already Exists` |

### Callback: Merchant Pre-Onboarding Callback

After the merchant completes Momnt's onboarding UI and accepts Terms & Conditions, Momnt POSTs the finalized merchant data to your configured callback URL.

**Requirements:**
- A successful pre-onboarding POST must have occurred first.
- The merchant must complete the onboarding UI and accept Terms & Conditions.

**Callback authentication:** Momnt uses Basic Auth on the callback URL, with credentials you pre-share with Momnt.

**URL parameters** on the callback URL are fully optional and follow standard key/value format.
