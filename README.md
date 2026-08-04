# MagicBell (magicbell)

<!-- API-EVANGELIST-PROVENANCE:BEGIN -->
> ### About this repository
>
> **This is not our API.** This repository is an independent, third-party profile of a company's
> **publicly available** API surface, maintained by [API Evangelist](https://apievangelist.com).
> API Evangelist does not operate, host, resell, or support this company's APIs, and is not
> affiliated with or endorsed by the company unless stated on the profile.
>
> **Where the information came from.** Everything here is assembled from material a member of the
> public can reach with a browser and no credentials — the company's own website, developer portal
> and documentation, the specifications it publishes for public use (OpenAPI, AsyncAPI, JSON Schema,
> `apis.json`, `llms.txt` and similar), its public repositories, and its public status, pricing and
> changelog pages. **Nothing here is obtained by breaching a system, defeating an access control, or
> using credentials of any kind.**
>
> **The rating is an independent assessment.** The Kin Score and Agent Readiness rating are
> independently calculated scores of a company's *public* API artifacts, produced by API Evangelist
> against a published rubric. They are not certifications, endorsements, security assessments, or
> audits, and they score published artifacts — not the quality, safety, or security of the software.
>
> **Corrections, re-scores, and removal are free.** No partnership, contract, or purchase is
> required, and you do not need to justify the request.
>
> - **Something wrong?** Open an issue on this repository, or email
>   [info@apievangelist.com](mailto:info@apievangelist.com).
> - **Published something new?** Ask for a re-score and we will re-run the rating.
> - **Want the listing taken down?** Say so and we will honor it. The profile is reduced to your
>   company name, a factual description, and a link to your own site, and the company is recorded as
>   **unrated** — never scored zero for having asked.
>
> **Response times.** Acknowledgement within **one business day**; removal or restriction within
> **two business days**; corrections and re-scores within **five business days**.
>
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

MagicBell is a multichannel push notification infrastructure platform that enables developers to deliver in-app, email, mobile push, web push, SMS, Slack, and Microsoft Teams notifications through a single unified REST API. The platform provides a ready-made notification inbox component, built-in user preference management, smart delivery workflows with fallback rules, and full delivery observability with event logging and debugging. MagicBell handles all channel routing and token management so product teams can focus on building rather than maintaining notification infrastructure.

**APIs.json:** https://raw.githubusercontent.com/api-evangelist/magicbell/refs/heads/main/apis.yml

**Naftiko:** https://github.com/naftiko/fleet?utm_source=api-evangelist&utm_medium=readme&utm_campaign=magicbell-api-evangelist&utm_content=repo

---

## Tags

notifications, push notifications, in-app notifications, email, SMS, Slack, Microsoft Teams, webhooks, notification inbox, multichannel, mobile push, web push

---

## APIs

### MagicBell REST API v2

The primary MagicBell REST API (v2) for sending notifications, managing users, configuring delivery channels, creating broadcasts, defining workflows, and querying delivery events. Supports JWT-based authentication (Project JWT and User JWT) and returns 429 on rate limit exceeded.

- **Documentation:** https://www.magicbell.com/docs/api
- **Reference:** https://www.magicbell.com/docs/api/reference
- **Base URL:** https://api.magicbell.com/v2
- **OpenAPI Spec:** https://public.magicbell.com/specs/openapi.v2.json

### MagicBell REST API v1

The legacy MagicBell REST API (v1) for notification delivery, user management, and channel configuration. New integrations should use v2.

- **Documentation:** https://www.magicbell.com/docs/v1
- **Base URL:** https://api.magicbell.com

---

## Plans, Rate Limits, and FinOps

### Plans

| Plan | Cost | Deliveries/Month | Projects |
|------|------|-----------------|----------|
| Builder | Free | 1,000 | 1 |
| Startup | $249/month | 50,000 (+$0.0025/overage) | 5 |
| Enterprise | Custom | Unlimited | Unlimited |

Full plans detail: [plans/magicbell-plans-pricing.yml](plans/magicbell-plans-pricing.yml)

### Rate Limits

| API | Method Type | Limit |
|-----|-------------|-------|
| REST v2 | GET / OPTIONS / HEAD | 250 req/min |
| REST v2 | POST / PATCH / PUT / DELETE | 200 req/min |
| REST v1 | GET / OPTIONS / HEAD | 100 req/min |
| REST v1 | POST / PATCH / PUT / DELETE | 60 req/min |

HTTP 429 returned on limit exceeded. Idempotency-Key header supported (UUID, 24-hour cache).

Full rate limits detail: [rate-limits/magicbell-rate-limits.yml](rate-limits/magicbell-rate-limits.yml)

### FinOps

Billing model: freemium tiered with overage. Primary meter is per-delivery (one notification, one user, one channel = one delivery). Multi-channel sends multiply the count.

Full FinOps detail: [finops/magicbell-finops.yml](finops/magicbell-finops.yml)

---

## Timestamps

- **Created:** 2026-06-12
- **Modified:** 2026-06-12

---

## Common Properties

| Property | URL |
|----------|-----|
| Website | https://www.magicbell.com/ |
| Documentation | https://www.magicbell.com/docs |
| API Reference | https://www.magicbell.com/docs/api/reference |
| GitHub Organization | https://github.com/magicbell |
| LinkedIn | https://www.linkedin.com/company/magicbell |
| X / Twitter | https://x.com/magicbell_io |
| Blog | https://www.magicbell.com/blog |
| Pricing | https://www.magicbell.com/pricing |
| Status Page | https://status.magicbell.com/ |
| Changelog | https://github.com/orgs/magicbell/discussions/categories/product-changelog |
| SDKs & Libraries | https://www.magicbell.com/docs/libraries |
| Developer Tools | https://www.magicbell.com/tools |

---

## Maintainers

- **Kin Lane** — kin@apievangelist.com
