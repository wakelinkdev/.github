[🇬🇧 English](README.md) | [🇷🇺 Русский](README_RU.md)

# WakeLink

<div align="center">

<img src="https://raw.githubusercontent.com/wakelinkdev/.github/main/assets/wakelink-logo-white.svg" alt="WakeLink Logo" width="200">

### Secure Remote Computer Management

[![Protocol](https://img.shields.io/badge/protocol-EWSP%20v1.0-6366f1?style=for-the-badge)](https://github.com/wakelinkdev/ewsp)
[![Encryption](https://img.shields.io/badge/encryption-XChaCha20-10b981?style=for-the-badge)](https://github.com/wakelinkdev/ewsp)
[![License](https://img.shields.io/badge/license-NGC%20v1.0-f59e0b?style=for-the-badge)](LICENSE)

[Documentation](https://wakelink-project.org/docs) • [Quick Start](#-quick-start) • [Contributing](https://github.com/wakelinkdev/.github/blob/main/CONTRIBUTING.md)

</div>

---

## About

**WakeLink** is a secure system for remote computer management with end-to-end encryption. Wake up your devices from anywhere with military-grade cryptography.

### Features

- 🖥️ **Wake-on-LAN** — Wake devices over the network
- 🔐 **End-to-End Encryption** — XChaCha20 + HMAC-SHA256
- 🌐 **Dual Mode** — Local TCP or Cloud WebSocket (TLS)
- ⛓️ **Replay Protection** — Blockchain-based packet chaining
- 🔑 **Forward Secrecy** — Session keys with rotation

---

## Repositories

<table>
<tr>
<td width="50%">

### 🔧 Core

| Repository | Description |
|:-----------|:------------|
| [**ewsp**][ewsp-core] | C cryptography library (EWSP protocol) |
| [**firmware**][firmware] | ESP8266/ESP32 firmware |

</td>
<td width="50%">

### 📱 Clients

| Repository | Platforms |
|:-----------|:----------|
| [**cli**][client] | Windows, macOS, Linux |
| [**android**][android] | Android 7.0+ |
| [**multiplatform**][kmp] | iOS, Android, Desktop |

</td>
</tr>
</table>

### 📚 Resources

| Repository | Description |
|:-----------|:------------|
| [**docs**][docs] | Documentation → [wakelink-project.org/docs](https://wakelink-project.org/docs) |

[ewsp-core]: https://github.com/wakelinkdev/ewsp
[firmware]: https://github.com/wakelinkdev/firmware
[client]: https://github.com/wakelinkdev/cli
[android]: https://github.com/wakelinkdev/android
[kmp]: https://github.com/wakelinkdev/multiplatform
[docs]: https://github.com/wakelinkdev/docs

---

## 🚀 Quick Start

```bash
# Install CLI
pip install cli

# Discover devices
wakelink scan

# Pair device
wakelink pair 192.168.1.100

# Wake your PC
wakelink wake
```

---

## 🏗️ Architecture

```
┌──────────────────────────────────────────────────────────────────┐
│                           CLIENTS                                 │
│   ┌─────────┐   ┌─────────┐   ┌─────────┐   ┌─────────────────┐  │
│   │   CLI   │   │ Android │   │   iOS   │   │     Desktop     │  │
│   └────┬────┘   └────┬────┘   └────┬────┘   └────────┬────────┘  │
│        └─────────────┴─────┬───────┴─────────────────┘           │
│                            ▼                                      │
│                ┌───────────────────────┐                         │
│                │      ewsp-core        │                         │
│                │  XChaCha20 + HMAC     │                         │
│                └───────────┬───────────┘                         │
└────────────────────────────┼─────────────────────────────────────┘
                             │
              ┌──────────────┴──────────────┐
              ▼                             ▼
       ┌─────────────┐             ┌────────────────┐
       │   TCP:99    │             │  WSS (Cloud)   │
       │   Local     │             │  wakelink.io   │
       └──────┬──────┘             └───────┬────────┘
              │                            │
              └────────────┬───────────────┘
                           ▼
                  ┌─────────────────┐
                  │    ESP8266/32   │
                  │    Firmware     │
                  └─────────────────┘
```

---

## 🔒 Security

| Feature | Description |
|:--------|:------------|
| **XChaCha20** | Stream cipher with 24-byte nonce |
| **HMAC-SHA256** | Packet authentication |
| **HKDF** | Key derivation with separation |
| **Blockchain Chain** | Replay attack protection |
| **Forward Secrecy** | Session keys with rotation |
| **Constant-Time** | Timing attack protection |

---

## 🤝 Contributing

We welcome contributions! See our [Contributing Guide](https://github.com/wakelinkdev/.github/blob/main/CONTRIBUTING.md) for details.

**Security issues?** Please email security@wakelink.io instead of opening a public issue.

---

## 📄 License

WakeLink is licensed under the **NGC v1.0** license.  
For commercial licensing inquiries, contact: license@wakelink.io

---

<div align="center">

**[Website](https://wakelink-project.org)** • **[Documentation](https://wakelink-project.org/docs)** • **[Discord](https://discord.gg/wakelink)**

Made with ❤️ by [@deadboizxc](https://github.com/deadboizxc)

</div>
