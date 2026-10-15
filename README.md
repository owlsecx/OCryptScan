# 🦉 OCryptScan

<p align="center">
  <img src="https://img.shields.io/badge/Platform-Linux-0a0c10?style=flat-square"/>
  <img src="https://img.shields.io/badge/Category-OCipher-blue?style=flat-square"/>
  <img src="https://img.shields.io/badge/License-MIT-green?style=flat-square"/>
  <img src="https://img.shields.io/badge/Part%20of-OwlSec%20Toolkit-7b5ea7?style=flat-square"/>
  <img src="https://img.shields.io/badge/Version-1.0.0-cyan?style=flat-square"/>
</p>

> **OCryptScan** — Weak-Cryptography Source Auditor

---

> ⚠️ **AUTHORISED USE ONLY** — Use only on systems you own or have explicit written permission to test. Unauthorised use is illegal.

---

## 📌 Overview

Weak-Cryptography Source Auditor

---

## ✨ Features

- Crypto-focused static analyser (SAST) for source code and configuration — Python, Java/Kotlin, JavaScript/TypeScript, Go, PHP, C#, C/C++, Ruby, YAML / JSON / XML / INI / .env / properties
- Broken hashes (MD2/MD4/MD5/SHA-1) with context heuristics: checksum / cache-key use is downgraded, password / signature / token use is escalated
- Weak ciphers — DES, 3DES, RC2, RC4, Blowfish, ECB, CBC without MAC, static / zero IVs, fixed nonces
- Weak key sizes — RSA / DSA / DH < 2048, EC < 256, AES-128 informational, short HMAC keys
- Insecure randomness in security context (random, Math.random, java.util.Random, rand, mt_rand ...)
- Hardcoded keys / secrets / passwords / IVs / salts, embedded PEM private keys, entropy scoring
- Weak password hashing — plain digests, missing bcrypt/scrypt/argon2/PBKDF2, low iteration counts, low bcrypt cost, static salts
- Insecure TLS code — verify=False, InsecureSkipVerify, trust-all managers, NODE_TLS_REJECT_UNAUTHORIZED=0, SSLv2/SSLv3/TLS1.0/1.1 forced, weak cipher strings
- Risky crypto APIs — unverified SSL contexts, Java Cipher.getInstance("AES") default ECB, PHP mcrypt, openssl_encrypt without IV, deprecated createCipher
- JWT 'none' algorithm, disabled signature checks, weak HMAC secrets
- CWE / OWASP / MITRE ATT&CK tags + concrete fix
- A+ … F crypto-posture grade with category subscores
- Inline '# nocrypt' suppression, allowlist, baseline
- Export TXT / Markdown / JSON / CSV / SARIF 2.1.0

---

## ⚙️ Requirements

- **Linux**
- **No Python installation needed** — runs as a standalone executable

---

## 🚀 Usage

```bash
./OCryptScan
```

---

## 📦 Part of OwlSec Toolkit

This tool is part of the **OwlSec** suite — a collection of 300+ security and privacy tools.

🔗 [owlsec.org](https://owlsec.org)

---

## ©️ License

MIT License — © Khaled S. Haddad

*Tools are distributed as pre-built executables. Source code is proprietary.*
