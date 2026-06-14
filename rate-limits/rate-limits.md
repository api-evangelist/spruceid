# SpruceID Rate Limits

SpruceID's open-source libraries and tooling are self-hosted by operators,
meaning rate limits are not imposed by SpruceID centrally. Instead, rate
limiting is the responsibility of the deploying organization.

## Self-Hosted Deployments (DIDKit HTTP, SIWE-OIDC, etc.)

SpruceID explicitly documents that **DIDKit HTTP does not implement any endpoint
authorization or access control**. The official guidance is:

> "A deployment should place DIDKit HTTP behind a reverse proxy with appropriate
> settings to limit access to its endpoints."

Recommended approaches for operators:
- Place behind an NGINX or Caddy reverse proxy with rate-limit rules
- Use Cloudflare or similar CDN/WAF for request throttling
- Implement API key authentication at the proxy layer
- Apply per-IP or per-client request limits based on expected credential
  issuance / verification volumes

## SIWE-OIDC (OpenID Connect Provider)

- No built-in rate limits documented
- Supports deployment on Cloudflare Workers (subject to Cloudflare's own
  request limits per plan) or as a standalone Rust binary
- Redis backend for session storage; connection pool limits apply

## Government / Enterprise Contracts

Rate limits and SLA guarantees for managed SpruceID infrastructure (Identity
Gateway, Digital IDs, Identity Wallet deployments) are defined per contract.
Contact hello@spruceid.com for details.

## Notes

- No publicly documented API call quotas, burst limits, or throttling policies
- Cryptographic operations (VC issuance, verification) are computationally
  bounded; production deployments should account for CPU and memory headroom
- The SpruceKit Showcase app (Google Play / App Store) is a demo/reference
  implementation with no defined SLA
