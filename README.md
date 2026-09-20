# Optimus Digital Lab

Canonical source repository for the Optimus Digital Lab storefront at https://store.techoptimus.net.

## Production guardrails

- Official commercial identity: **info@techoptimus.net**
- Current public launch prices:
  - AI Visibility GEO Prompt System — **USD 9.95**
  - Luxury Jewelry AI Product Photography System — **USD 11.95**
  - Jewelry AI Shot Planner — **USD 4.95**
- Never commit payment/API secrets.
- Never commit paid customer bundles or private buyer-delivery assets.
- Never publish a product unless post-payment delivery has been verified end to end.
- Whop products/plans remain hidden until delivery reliability is proven.

## Deployment strategy

Current production runs on AppDeploy. This repository is intended to become the provider-neutral source of truth, with a Cloudflare failover/secondary deployment lane so AppDeploy deployment-credit limits do not block urgent fixes.

The production migration gate is:

`storefront -> checkout -> payment verification -> private delivery -> funnel recording`

Do not switch DNS or publish hidden products until every gate passes.
