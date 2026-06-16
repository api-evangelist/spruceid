# SpruceID (spruceid)

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
