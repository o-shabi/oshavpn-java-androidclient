# 📡 OshaVPN — Android Client

A **feature-rich, API-driven VPN client** for Android, written entirely in **Java**.  
OshaVPN loads servers, operators, protocols, and subscription plans dynamically from a remote API and supports multiple tunneling protocols via native `.so` libraries.

> ✅ Previously production-grade — now open-sourced for community development and modernisation.

---

## ✨ Features

| Category | Details |
|----------|---------|
| 🔐 **Account System** | Full signup, login, and session handling |
| 🌐 **Dynamic Backend** | Servers, operators, and available clients are fetched live from the API |
| 📡 **Multi-Protocol** | OpenVPN · OpenConnect (Cisco AnyConnect) · IKEv2 · SOCKS5 · Custom Tunnel |
| 💳 **Subscription Plans** | Managed and verified entirely through the API — no third‑party billing SDKs |
| ⚡ **One-Tap Control** | Simple connect / disconnect with status feedback |
| 🚪 **Clean Exit** | Disconnect VPN and log out in a single flow |

---

## 📦 Project Status

This app was **fully functional and used in production** approximately three years ago.  
It is currently **unmaintained** and shared as a **reference implementation** for developers.

> ⚠️ Before considering production use, please **audit all dependencies**, update to modern Android API levels, and review the bundled native libraries.

---

## 🧱 Architecture

OshaVPN follows a **thin‑client model**:

- 📲 **Android UI (Java)** – handles user interaction
- ☁️ **Remote API** – provides all dynamic configuration (servers, operators, plans)
- 🔧 **Native libraries (`.so`)** – handle the actual VPN tunnels for each protocol

No sensitive logic is hardcoded — the backend fully controls the client's behaviour.

---

## 👥 Intended Audience

This repo is for **developers** who want to:

- 🔍 Study a real‑world Android VPN implementation in Java
- 🔗 Adapt the client to their own backend API
- 🛠️ Modernise and extend the codebase (Kotlin, Jetpack Compose, etc.)
- 🧱 Use it as a **foundation** for a new VPN project

---

## 🚀 Getting Started

### ✅ Prerequisites

- [Android Studio](https://developer.android.com/studio) (latest stable recommended)
- Android SDK matching the project's `targetSdkVersion`
- NDK setup (only if you need to rebuild the native `.so` libraries)

### 🔧 Build Instructions

1. Clone the repository
```bash
git clone https://github.com/o-shabi/oshavpn-java-androidclient.git
```
2. Open the project in Android Studio
3. Configure the API endpoint. Look in: app/src/main/res/values/strings.xml (or a dedicated config file)
4. Build and run on a device or emulator

---

## 📄 License

This project is licensed under the **GNU General Public License v3.0 (GPL v3)**
This ensures compliance with the licensing of the bundled native VPN protocol libraries and guarantees that all derivative works remain open source.
See the [LICENSE](LICENSE) file for details.

---

Made with ☕ and a lot of packets 📨
