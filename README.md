# SpruceID (spruceid)

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

SpruceID is a decentralized identity company providing open-source tools and infrastructure for governments and enterprises to issue, verify, and manage digital identity credentials. Their platform supports W3C Verifiable Credentials, Decentralized Identifiers (DIDs), OpenID for Verifiable Credential Issuance (OID4VCI), OpenID for Verifiable Presentations (OID4VP), Sign-In with Ethereum (SIWE), and ISO/IEC 18013-5 mobile driver's licenses (mDL). SpruceID's SpruceKit toolkit enables developers to build wallet apps, credential issuers, and verifier integrations using standards-based identity protocols.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/spruceid/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/spruceid/refs/heads/main/apis.yml)

## Tags

- Decentralized Identity
- Verifiable Credentials
- DIDs
- Sign-In with Ethereum
- Identity Wallet
- Government
- OpenID Connect
- W3C Standards

## Timestamps

- **Created:** 2026-06-14
- **Modified:** 2026-06-14

## APIs

### SpruceID DIDKit HTTP API

DIDKit is SpruceID's cross-platform toolkit for working with W3C Decentralized Identifiers (DIDs) and Verifiable Credentials (VCs). The DIDKit HTTP server exposes REST endpoints for issuing, presenting, and verifying verifiable credentials and verifiable presentations using standard cryptographic proofs. It implements the W3C VC API specification and supports multiple DID methods including did:key, did:web, did:ethr, and did:tz. Note: DIDKit HTTP does not include built-in authorization and should be deployed behind a reverse proxy in production.

- **Human URL:** [https://spruceid.dev/docs/didkit/](https://spruceid.dev/docs/didkit/)
- **Base URL:** `https://localhost:8080`

#### Tags

- Verifiable Credentials
- DIDs
- W3C VC API
- Credential Issuance
- Credential Verification

#### Properties

- [Documentation](https://spruceid.dev/docs/didkit/)
- [GitHub Repository](https://github.com/spruceid/didkit-http)
- [OpenAPI](https://raw.githubusercontent.com/spruceid/didkit-http/main/openapi.yaml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)

### SpruceID Sign-In with Ethereum (SIWE) API

Sign-In with Ethereum (SIWE) enables Ethereum accounts to authenticate with off-chain services by signing a standardized message format (EIP-4361). SpruceID's SIWE library provides client and server implementations in TypeScript for integrating Ethereum wallet-based authentication into web applications. The SIWE-OIDC component wraps SIWE in an OpenID Connect Identity Provider, enabling drop-in integration with OAuth 2.0 and OIDC flows. Supported wallets include MetaMask, Coinbase Wallet, and any WalletConnect-compatible wallet. ENS domain resolution is included for human-readable usernames.

- **Human URL:** [https://eips.ethereum.org/EIPS/eip-4361](https://eips.ethereum.org/EIPS/eip-4361)
- **Base URL:** `https://oidc.spruceid.com`

#### Tags

- Authentication
- Sign-In with Ethereum
- SIWE
- OpenID Connect
- Ethereum
- Blockchain Identity

#### Properties

- [Documentation](https://spruceid.dev/docs/)
- [GitHub Repository](https://github.com/spruceid/siwe)
- [GitHub Repository](https://github.com/spruceid/siwe-oidc)
- [N P M Package](https://www.npmjs.com/package/siwe)

### SpruceID SSI Core Library API

The SpruceID SSI (Self-Sovereign Identity) core library provides a comprehensive Rust API for signing, issuing, and verifying W3C Verifiable Credentials and JSON Web Tokens. It supports VC Data Model 1.1 and 2.0, JWT-VC, Data Integrity proofs, BBS+ selective disclosure, and a wide range of cryptographic signature suites including EdDSA, secp256k1, P-256, and more. The library has undergone a Trail of Bits security audit and serves as the foundation for DIDKit and other SpruceID tooling.

- **Human URL:** [https://github.com/spruceid/ssi](https://github.com/spruceid/ssi)
- **Base URL:** `https://crates.io/crates/ssi`

#### Tags

- Verifiable Credentials
- DIDs
- Cryptography
- W3C Standards
- Rust Library
- JWT
- Selective Disclosure

#### Properties

- [Documentation](https://docs.rs/ssi/)
- [GitHub Repository](https://github.com/spruceid/ssi)
- [Rust Crate](https://crates.io/crates/ssi)

### SpruceID OID4VCI Credential Issuance API

SpruceID's OID4VCI (OpenID for Verifiable Credential Issuance) Rust library implements the OpenID4VC credential issuance protocol, enabling credential issuers to deliver W3C Verifiable Credentials to holder wallets. The protocol extends OAuth 2.0 with credential endpoint flows including pre-authorized code flow and authorization code flow. Supported credential formats include JWT-VC, LDP-VC, SD-JWT VC, and ISO/IEC 18013-5 mobile documents (mDL). Used as the issuance layer in the SpruceKit mobile SDK.

- **Human URL:** [https://github.com/spruceid/oid4vci-rs](https://github.com/spruceid/oid4vci-rs)
- **Base URL:** `https://openid.net/specs/openid-4-verifiable-credential-issuance-1_0.html`

#### Tags

- Credential Issuance
- OID4VCI
- OpenID Connect
- Verifiable Credentials
- mDL
- OAuth 2.0

#### Properties

- [Documentation](https://www.sprucekit.dev/)
- [GitHub Repository](https://github.com/spruceid/oid4vci-rs)
- [Specification](https://openid.net/specs/openid-4-verifiable-credential-issuance-1_0.html)

### SpruceID OID4VP Verifiable Presentations API

SpruceID's OID4VP (OpenID for Verifiable Presentations) Rust library implements the OpenID4VC credential presentation protocol, enabling verifier applications to request and receive verifiable credentials from holder wallets. The library handles presentation definitions, selective disclosure, and cryptographic proof verification. Supported credential formats include JWT-VC, LDP-VC, SD-JWT VC, and ISO/IEC 18013-5 mobile driver's licenses (mDL) for offline presentation. Integrates with SpruceKit mobile SDKs for iOS and Android wallet apps.

- **Human URL:** [https://github.com/spruceid/openid4vp](https://github.com/spruceid/openid4vp)
- **Base URL:** `https://openid.net/specs/openid-4-verifiable-presentations-1_0.html`

#### Tags

- Credential Verification
- OID4VP
- OpenID Connect
- Verifiable Presentations
- mDL
- Privacy-Preserving

#### Properties

- [Documentation](https://www.sprucekit.dev/)
- [GitHub Repository](https://github.com/spruceid/openid4vp)
- [Specification](https://openid.net/specs/openid-4-verifiable-presentations-1_0.html)

### SpruceID isomdl Mobile Driver's License API

SpruceID's isomdl library provides a Rust implementation of the ISO/IEC 18013-5 standard for mobile driver's licenses (mDL). It enables issuers to create standards-compliant mDL credentials and verifiers to request and validate presentations both online and in offline (proximity) scenarios. The library is integrated into SpruceKit mobile SDKs for iOS and Android, supporting real-world deployment of government-issued digital identity documents.

- **Human URL:** [https://github.com/spruceid/isomdl](https://github.com/spruceid/isomdl)
- **Base URL:** `https://crates.io/crates/isomdl`

#### Tags

- Mobile Driver's License
- mDL
- ISO 18013-5
- Government Identity
- Offline Verification

#### Properties

- [Documentation](https://www.sprucekit.dev/)
- [GitHub Repository](https://github.com/spruceid/isomdl)
- [Rust Crate](https://crates.io/crates/isomdl)

## Common Properties

- [Website](https://spruceid.com)
- [Developer](https://www.sprucekit.dev/)
- [Blog](https://blog.spruceid.com)
- [Git Hub](https://github.com/spruceid)
- [Knowledge Base](https://learn.spruceid.com)
- [Privacy Policy](https://spruceid.com/privacy)
- [Contact](https://spruceid.com/contact)
- [Discord](https://discord.gg/spruceid)

## Maintainers

**FN:** SpruceID
**Email:** hello@spruceid.com
