---
title: Merchant Users
description: Create and manage users for a merchant
---

## Create Merchant User

`POST /api/v1/sponsor/merchants/users/`

Creates a new user for a merchant. The fields provided are checked against the Momnt database to verify permissions and accounts exist.

**Requirements:**
- A merchant must already exist before users can be created.
- Users are created by Admin users — one must exist.
- A successful merchant onboarding workflow must have occurred before this endpoint can be used.

---

## Update Merchant User

`PATCH /api/v1/sponsor/merchants/users/{user_id}/` *(or similar — see API reference)*

Updates an existing merchant user's details.

---

## Batch Create Merchant Users

`POST /api/v1/sponsor/merchants/users/batch/` *(or similar — see API reference)*

Creates multiple merchant users in a single request.

**Use this endpoint** when you need to bulk-provision users during merchant setup.
