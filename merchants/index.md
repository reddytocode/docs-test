---
title: Merchants
description: Overview of merchant management endpoints in the Belle Sponsor API
---

## Overview

The Merchant APIs allow sponsors to manage the full lifecycle of a merchant on the platform — from initial onboarding through payment setup, rate sheet configuration, offer codes, and user management.

## Endpoints

| Group | Description |
|---|---|
| [Onboarding](onboarding.md) | Invite merchants to apply and complete account creation |
| [Payment Details](payment-details.md) | Add or update bank account details, initiate and verify micro-deposits |
| [Rate Sheets](rate-sheets.md) | View and update the loan products available to a merchant |
| [Offer Codes](offer-codes.md) | Create and manage promotional offer codes for a merchant |
| [Statements](statements.md) | Retrieve merchant billing statements |
| [Users](users.md) | Create and update merchant users |

## Authentication

All merchant endpoints require Basic Auth. The authenticated sponsor's ID is used to scope all operations — you can only manage merchants associated with your sponsor account.
