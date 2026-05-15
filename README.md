# Casket

[![CI](https://github.com/CarriedWorldUniverse/casket-ts/actions/workflows/ci.yml/badge.svg?branch=main)](https://github.com/CarriedWorldUniverse/casket-ts/actions/workflows/ci.yml)
[![Release](https://img.shields.io/github/v/release/CarriedWorldUniverse/casket-ts?include_prereleases&sort=semver&display_name=tag)](https://github.com/CarriedWorldUniverse/casket-ts/releases)
[![License](https://img.shields.io/github/license/CarriedWorldUniverse/casket-ts)](LICENSE)

Small, easy-to-use authenticated encryption library for TypeScript / Node.js / Cloudflare Workers.

- **AES-256-GCM** and **ChaCha20-Poly1305** with Argon2id key derivation
- **Channel** module: Ed25519/P-256 identity + ECDH E2E encryption for frame-to-frame relay
- Cross-compatible wire format with [@nexus-cw/casket](https://github.com/nexus-cw/casket-ts) (Node.js / Cloudflare Workers)
- Targets `netstandard2.1`, `net8.0`, `net9.0`, `net10.0`

## Install

```
dotnet add package Casket
```

## License

MIT
