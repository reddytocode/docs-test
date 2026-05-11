---
title: Consumers
description: Overview of consumer-facing endpoints in the Belle Sponsor API
---

## Overview

The Consumer APIs allow sponsors to initiate loan applications, run soft credit pulls, manage transactions, and process payments and refunds on behalf of consumers.

## Endpoints

| Group | Description |
|---|---|
| [Applications](applications.md) | Invite a consumer to apply for a loan via SMS or email |
| [Soft Pull](soft-pull.md) | Run a soft credit pull and return available loan offers |
| [Transactions](transactions.md) | View transaction activity, available transactions, and settled charges |
| [Payment Requests](payment-requests.md) | Create and list consumer payment requests |
| [Refunds](refunds.md) | Initiate consumer refund requests |

## Authentication

All consumer endpoints require Basic Auth. The Sponsor ID is determined by the credentials used.
