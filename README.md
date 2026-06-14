# Sezzle

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
