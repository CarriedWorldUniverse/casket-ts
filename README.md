# Casket

[![CI](https://github.com/CarriedWorldUniverse/casket-ts/actions/workflows/ci.yml/badge.svg?branch=main)](https://github.com/CarriedWorldUniverse/casket-ts/actions/workflows/ci.yml)
[![Release](https://img.shields.io/github/v/release/CarriedWorldUniverse/casket-ts?include_prereleases&sort=semver&display_name=tag)](https://github.com/CarriedWorldUniverse/casket-ts/releases)
[![License](https://img.shields.io/github/license/CarriedWorldUniverse/casket-ts)](LICENSE)

Small, easy-to-use authenticated encryption library for TypeScript / Node.js / Cloudflare Workers.

- **AES-256-GCM** and **ChaCha20-Poly1305** with Argon2id key derivation
- **Channel** module: Ed25519/P-256 identity + ECDH E2E encryption for frame-to-frame relay
- Cross-compatible wire format with the .NET Casket implementation
- Runs on Node.js (>=18) and Cloudflare Workers

## Install

```
npm install @nexus-cw/casket
```

## Usage

```ts
import { sealWithPassword, unsealWithPassword } from '@nexus-cw/casket';

const token = await sealWithPassword('secret message', 'correct horse battery staple');
const plaintext = await unsealWithPassword(token, 'correct horse battery staple');
```

Key-based sealing (synchronous, raw key) is also available:

```ts
import { generateKey, sealWithKey, unsealWithKey, keySourceFromBuffer } from '@nexus-cw/casket';

const key = generateKey();
const source = keySourceFromBuffer(Buffer.from(key, 'base64url'));
const token = sealWithKey('secret message', source);
const plaintext = unsealWithKey(token, source);
```

## Develop

```
npm install
npm run build
npm test
```

## License

MIT
