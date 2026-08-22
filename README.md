# Sezzle

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
> **Not from the company, and here with a question?** You are welcome here — we would rather be the
> front line and point you the right way than have a good report go nowhere. What this repository
> can answer is narrow, though, so it is worth knowing who you are actually looking for:
>
> - **A question about how the API works, an account, billing, or a bug in the service** — that is
>   the company's own support, not us. We profile this API; we do not operate it and cannot see
>   your account.
> - **A bug in an open-source project we only catalog** — file it on that project's own repository.
>   This has happened with a real and correct bug report that reached us instead of the people who
>   could fix it, which helped nobody.
> - **Anything about this listing itself** — the description, the tags, the rating, a missing or
>   wrong artifact — is ours. Open an issue here.
> - **Not sure, or something general about API Evangelist or APIs.io** — open an issue on the
>   [APIs.io Inbox](https://github.com/api-search/inbox) and we will route it.
>
> **This repository contains no software, and we will never ask you to download anything.** There is
> no build, release, installer, or binary here — only text and machine-readable API descriptions, so
> there is nothing here that can be "corrupt" or need "repairing". Any issue, comment, or email
> claiming otherwise and offering a download link is not from us and is hostile. Do not follow the
> link; it is a lure. Report it to GitHub and, if you like, tell us at
> [info@apievangelist.com](mailto:info@apievangelist.com) so we can take it down.
>
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

Sezzle is a buy-now-pay-later (BNPL) platform that enables merchants to offer installment payment options at checkout. Shoppers split purchases into four interest-free payments over six weeks. This repository contains the APIs.json 0.19 profile for Sezzle's public merchant APIs.

## APIs

| API | Version | Base URL |
|-----|---------|----------|
| Sezzle API v2 | 2.0.0 | `https://gateway.sezzle.com/v2` |
| Sezzle API v1 | 1.0 (legacy) | `https://gateway.sezzle.com/v1` |

## Key Resources

- **Developer Docs:** https://docs.sezzle.com/docs/api/intro
- **OpenAPI Spec (v2):** https://gateway.sezzle.com/v2api.yaml
- **Sandbox:** `https://sandbox.gateway.sezzle.com/v2`
- **Merchant Dashboard:** https://dashboard.sezzle.com/merchant
- **Merchant Support:** https://merchant-help.sezzle.com
- **GitHub:** https://github.com/sezzle

## Authentication

Sezzle uses API key-based bearer token authentication. Merchants obtain a short-lived bearer token by posting their `public_key` and `private_key` to `POST /v2/authentication`. All subsequent API requests include the token in the `Authorization: Bearer <token>` header.

## Core Capabilities

- **Checkout Sessions** — Create redirect-based checkout sessions for Pay in 4 installments
- **Order Management** — Capture, refund, release, reauthorize, and upcharge orders
- **Customer Tokenization** — Save shopper payment methods for recurring or one-click purchases
- **Webhooks** — Register and manage webhook endpoints for order and customer lifecycle events
- **Settlement Reporting** — Access payout summaries and detailed settlement CSV exports
- **Interest Accounts** — Check balance and activity for merchant interest accounts

## Merchant Fees

- **Transaction Fee:** ~6% + $0.30 per order (rates vary by merchant)
- **Monthly Minimum:** $15 USD if less than $300 processed in a 30-day period
- **Setup Fee:** None

## SDKs and Integrations

- Node.js SDK: https://github.com/sezzle/sezzle-node
- Android SDK: https://github.com/sezzle/sezzle-merchant-sdk-android
- iOS SDK: https://github.com/sezzle/sezzle-merchant-sdk-ios
- Magento 2: https://github.com/sezzle/sezzle-magento2
- Shopify: https://apps.shopify.com/sezzle-payments

## Maintainer

[API Evangelist](https://apievangelist.com) — kin@apievangelist.com
