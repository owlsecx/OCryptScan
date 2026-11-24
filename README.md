# 🦉 OCryptScan

<p align="center">
  <img src="https://img.shields.io/badge/Platform-Linux-0a0c10?style=flat-square"/>
  <img src="https://img.shields.io/badge/Category-OCipher-blue?style=flat-square"/>
  <img src="https://img.shields.io/badge/License-Proprietary-orange?style=flat-square"/>
  <img src="https://img.shields.io/badge/Part%20of-OwlSec%20Toolkit-7b5ea7?style=flat-square"/>
  <img src="https://img.shields.io/badge/Version-1.0.0-cyan?style=flat-square"/>
</p>

> **OCryptScan** — Weak-Cryptography Source Auditor

---

> ⚠️ **AUTHORISED USE ONLY** — Use only on systems you own or have explicit written permission to test. Unauthorised use is illegal.

---

## 📌 Overview

OCryptScan — Weak-Cryptography Source Auditor. It provides crypto-focused static analyser (SAST) for source code and configuration — Python, Java/Kotlin, JavaScript/TypeScript, Go, PHP, C#, C/C++, Ruby, YAML / JSON / XML / INI / .env / properties. Operators can export results (including machine-readable formats) and gate CI with severity thresholds where supported.

---

## ✨ Features

- Crypto-focused static analyser (SAST) for source code and configuration — Python, Java/Kotlin, JavaScript/TypeScript, Go, PHP, C#, C/C++, Ruby, YAML / JSON / XML / INI / .env / properties
- Broken hashes (MD2/MD4/MD5/SHA-1) with context heuristics: checksum / cache-key use is downgraded, password / signature / token use is escalated
- Weak ciphers — DES, 3DES, RC2, RC4, Blowfish, ECB, CBC without MAC, static / zero IVs, fixed nonces
- Weak key sizes — RSA / DSA / DH < 2048, EC < 256, AES-128 informational, short HMAC keys
- Insecure randomness in security context (random, Math.random, java.util.Random, rand, mt_rand ...)
- Hardcoded keys / secrets / passwords / IVs / salts, embedded PEM private keys, entropy scoring

---

## ⚙️ Requirements

- **Linux**
- **No Python installation needed** — runs as a standalone executable

---

## 🚀 Usage

```bash
./OCryptScan                                     # interactive menu
./OCryptScan --path ./config_or_ruleset
./OCryptScan --json -o report.json
./OCryptScan --help
```

---

## 📦 Part of OwlSec Toolkit

This tool is part of the **OwlSec** suite — a collection of 275+ security and privacy tools.

🔗 [owlsec.org](https://owlsec.org)

---

## ©️ License

Proprietary — © 2026 Owlsec LLC. All rights reserved.

*Tools are distributed as pre-built executables. Source code is proprietary.*

---

## 🔍 Verification & Transparency

This tool is closed-source. These files let you see exactly what is inside it,
without the source:

- [`SBOM.cdx.json`](SBOM.cdx.json) — CycloneDX inventory: SHA-256 of this
  binary, bundled CPython version, and every bundled library with its exact
  version and license. Feed it to Grype, Trivy or Dependency-Track to audit
  our dependencies for CVEs yourself.
- [`THIRD-PARTY-NOTICES.md`](THIRD-PARTY-NOTICES.md) — the full license text
  of every third-party component, extracted from this binary.

**No telemetry, no analytics, no licence check-in.** This tool does not phone
home. Verify that claim yourself:

```bash
sudo strace -f -e trace=network ./OCryptScan --help   # watch every network call
firejail --net=none ./OCryptScan --help               # deny the network entirely
```

Release signing, GPL compliance and vulnerability reporting:
[**TRUST.md**](https://github.com/owlsecx/owl-os/blob/main/TRUST.md)
