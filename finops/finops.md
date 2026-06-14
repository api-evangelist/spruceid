# SpruceID FinOps

## Cost Model

SpruceID operates an open-source / government-contract hybrid model. There are
no metered API calls or per-credential fees for the self-hosted open-source
stack. Cost drivers are infrastructure and professional services.

## Open Source Stack — Operator Cost Drivers

| Component | Hosting Cost Driver |
|---|---|
| DIDKit HTTP | Server/container hosting; scales with VC issuance volume |
| SSI Library | Build-time dependency; no runtime hosting cost |
| SIWE TypeScript | CDN/NPM delivery; negligible |
| SIWE-OIDC | Cloudflare Workers (per-request billing) or VPS/Kubernetes |
| OID4VCI / OID4VP | Rust binary hosting; scales with credential flows |
| isomdl | Embedded in mobile apps; no separate hosting cost |
| SpruceKit Mobile SDK | App store distribution; no direct hosting cost |

### Cloudflare Workers (SIWE-OIDC)

If deploying SIWE-OIDC on Cloudflare Workers:
- **Free plan:** 100,000 requests/day
- **Paid plan (Workers Paid):** $5/month + $0.50 per million requests beyond 10M
- Redis-compatible KV storage billed separately

### Infrastructure Estimation (Self-Hosted DIDKit HTTP)

| Scale | Recommended Instance | Est. Monthly Cost |
|---|---|---|
| Development / low volume | 1 vCPU, 1 GB RAM | ~$5–15/mo (VPS) |
| Production (1K creds/day) | 2 vCPU, 4 GB RAM | ~$20–50/mo |
| High throughput (10K+ creds/day) | Horizontal scaling, load balancer | Variable |

## Enterprise / Government Contracts

SpruceID's primary revenue comes from government identity infrastructure
contracts. Pricing is not publicly disclosed and is negotiated per engagement.

Typical engagement scope may include:
- Initial implementation and integration (professional services)
- Ongoing hosting and managed infrastructure
- SLA-backed uptime guarantees
- Security and compliance advisory

Contact: hello@spruceid.com

## Cost Optimization Notes

- All core libraries are Apache-2.0 licensed — no licensing fees
- Cryptographic operations (EdDSA, P-256) are CPU-intensive; profile under
  expected load before sizing infrastructure
- mDL offline verification eliminates the need for real-time network calls
  during in-person verification, reducing operational latency and cost
- BBS+ selective disclosure reduces data transfer overhead per presentation

## No Public SaaS Pricing

As of June 2026, SpruceID does not offer a publicly priced SaaS API tier with
metered billing. All managed services are delivered through direct contracts.
