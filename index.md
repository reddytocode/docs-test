## Getting Started

Base URLS:
- Staging URL  `https://app-stg.momnt.com/`
- Production URL  `https://app.momnt.com/`
### Basic Authentication

All requests to the Momnt Sponsor API must be authenticated using **HTTP Basic Authentication**.  
You must include your **email (username)** and **API password** in the request using the `-u` flag or the `Authorization: Basic` header.

In Basic Authentication, the credentials are sent as `username:password` and encoded in Base64 by the client.

Below is an example request using `curl`:

```bash
curl -s -X POST "https://app-stg.momnt.com/api/v1/sponsor/consumers/soft-pull/" \
  -H "Content-Type: application/json" \
  -u "mail@test.com:pwd" \
  -d '{}'

```
