# OshaVPN - Android Client

An open-source, API-driven VPN client for Android, built entirely in Java. It supports multiple VPN protocols and loads servers, operators, and plans dynamically from a remote API. Previously production-grade, now released for community development.

## Features

- **Account System:** Signup, login, and session management.
- **Dynamic Content:** Servers, operators, and available VPN clients are loaded from a remote API.
- **Multi-Protocol Support:**
  - OpenVPN
  - OpenConnect (Cisco AnyConnect)
  - IKEv2
  - SOCKS Proxy
  - Custom Tunnel
- **Subscription Plans:** Plans are managed and verified through the API, with no third-party payment SDKs.
- **Connection Control:** Simple one-tap connect and disconnect.
- **Account Exit:** Disconnect and log out cleanly.

## Project Status

OshaVPN was a fully functional, production-used app about three years ago. It is now **unmaintained** and shared as a reference for developers. Before any production use, you should audit dependencies, update libraries, and adapt the code to current Android API levels and security standards.

## Architecture

The app is a thin client for a remote API. All configuration (servers, operators, protocols, plans) is fetched from the backend. Native VPN protocol libraries (bundled as `.so` files) handle the actual tunnel connections.

## Intended Audience

This repository is for **developers** who want to:
- Study a real-world Android VPN client implementation in Java.
- Adapt the client to their own backend API.
- Modernize and extend the codebase.
- Use it as a foundation for a new project.

## Getting Started

### Prerequisites
- Android Studio
- Android SDK (API level that matches the project's `targetSdkVersion`)
- NDK (if rebuilding native `.so` libraries)

### Build Instructions
1.  Clone the repository:
    ```bash
    git clone https://github.com/o-shabi/oshavpn-java-androidclient.git
    ```
2. Open the project in Android Studio.
3. Configure the API endpoint in the project settings (check app/src/main/res/values/strings.xml or a dedicated config file).
4. Build and run on a device or emulator.

## License

This project is licensed under the **GNU General Public License v3.0 (GPL v3)**. This choice respects the licensing terms of the bundled native VPN protocol libraries. All derivative works must also be open source under a GPL v3 compatible license.
See the [LICENSE](LICENSE) file for details.
