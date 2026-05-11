---
title: Getting Started
description: Overview and quick start for the Belle Sponsor API
---

## Overview

The Belle Sponsor API lets you manage merchants, issue consumer loans, and integrate embedded lending into your platform.

**Base URLs:**

| Environment | URL |
|---|---|
| Staging | `https://app-stg.momnt.com/` |
| Production | `https://app.momnt.com/` |

## Authentication

All requests require **HTTP Basic Authentication** — your email (username) and API password.

```bash
curl -s -X POST "https://app-stg.momnt.com/api/v1/sponsor/consumers/soft-pull/" \
  -H "Content-Type: application/json" \
  -u "mail@test.com:your-api-password" \
  -d '{}'
```

See [Authentication](authentication.md) for full details.

## API Sections

- **[Merchants](merchants/index.md)** — Onboard merchants, manage payment details, rate sheets, offer codes, and users.
- **[Consumers](consumers/index.md)** — Invite consumers, run soft pulls, manage applications, transactions, and refunds.
