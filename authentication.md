---
title: Authentication
description: How to authenticate with the Belle Sponsor API using HTTP Basic Auth
---

## HTTP Basic Authentication

All requests to the Belle Sponsor API must be authenticated using **HTTP Basic Authentication**. You must include your **email (username)** and **API password** in every request.

Credentials are sent as `username:password`, Base64-encoded, in the `Authorization` header. Most HTTP clients handle this automatically.

### Using curl

Pass credentials with the `-u` flag:

```bash
curl -s -X GET "https://app-stg.momnt.com/api/v1/sponsor/merchants/" \
  -H "Content-Type: application/json" \
  -u "mail@example.com:your-api-password"
```

### Using the Authorization header directly

```bash
curl -s -X GET "https://app-stg.momnt.com/api/v1/sponsor/merchants/" \
  -H "Content-Type: application/json" \
  -H "Authorization: Basic $(echo -n 'mail@example.com:your-api-password' | base64)"
```

## Environments

| Environment | Base URL |
|---|---|
| Staging | `https://app-stg.momnt.com/` |
| Production | `https://app.momnt.com/` |

Use staging for development and testing. API passwords differ between environments.

## Callback Authentication

Endpoints that fire callbacks (e.g., merchant onboarding, consumer applications) also support Basic Auth on the callback URL. You provide Momnt with a username and password, which Momnt stores securely and uses when POSTing to your callback URL.
