---
title: Merchant Payment Details
description: Add or update merchant bank account details and manage micro-deposit verification
---

## Add / Edit Merchant Payment Details

`POST /api/v1/sponsor/merchants/payment-detail/`

Add or update the bank account details for a merchant. This must be completed before a merchant can receive payouts.

---

## Initiate Micro-Deposits

`POST /api/v1/sponsor/merchants/payment-detail/initiate-micro-deposits/{request_user_id}/`

Re-initiates the micro-deposit verification process. Use this endpoint only after a verification failure — when `bank_account_status` is `VerificationFailed`.

This happens when a merchant exhausts their verification attempts (more than three wrong entries) or when micro-deposits expire (after 14 days).

**Requirements:**
- The `request_user_id` must have an Admin role on the account.
- No request body fields are required.

---

## Verify Micro-Deposits

`POST /api/v1/sponsor/merchants/payment-detail/verify-micro-deposits/{request_user_id}/`

Verifies the merchant's business bank account using two small deposits (between $0.01 and $0.99 inclusive).

Deposit amounts can be provided as floats or string representations of cents (e.g., `"0.75"`, `"0.01"`).

**Requirements:**
- The `request_user_id` must have an Admin role on the account.
- Authentication (username and password) is required; Sponsor ID is determined by the credentials used.
