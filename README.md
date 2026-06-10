# casket-ts

[![CI](https://github.com/CarriedWorldUniverse/casket-ts/actions/workflows/ci.yml/badge.svg?branch=main)](https://github.com/CarriedWorldUniverse/casket-ts/actions/workflows/ci.yml)
[![Release](https://img.shields.io/github/v/release/CarriedWorldUniverse/casket-ts?include_prereleases&sort=semver&display_name=tag)](https://github.com/CarriedWorldUniverse/casket-ts/releases)
[![License](https://img.shields.io/github/license/CarriedWorldUniverse/casket-ts)](LICENSE)

Small, easy-to-use authenticated encryption library for TypeScript / Node.js / Cloudflare Workers.

- **AES-256-GCM** and **ChaCha20-Poly1305** with Argon2id key derivation
- **Channel** module: Ed25519 identity + dual-curve ECDH (P-256 / X25519) for E2E encryption — pair-relay channels and at-rest envelopes
- Cross-compatible channel wire format with [casket-go](https://github.com/CarriedWorldUniverse/casket-go) (Go) and [casket-dotnet](https://github.com/CarriedWorldUniverse/casket-dotnet) (.NET)

## Install

```
npm install @nexus-cw/casket
```

## License

Apache-2.0. See [LICENSE](LICENSE).
