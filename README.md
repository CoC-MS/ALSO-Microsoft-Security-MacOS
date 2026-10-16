# 🛡️ ALSO Microsoft Security - macOS

> Microsoft Intune security policy exports and supporting artifacts for macOS devices, helping organizations accelerate secure deployments and apply Microsoft security best practices.

> [!IMPORTANT]
> These exports are starting points, not ready-made tenant configurations. Review licensing, settings, tenant-specific values, dependencies, and assignments; pilot policies before expanding deployment.

---

<a id="getting-started"></a>
## 🚀 Getting started

1. Review the [general prerequisites](docs/public/general-prerequisites.md), [macOS prerequisites](docs/public/macos-prerequisites.md), [dependencies and special handling](docs/public/dependencies-and-errors.md), [Defender for Cloud Apps/Defender for Business Custom Indicators and Web Content Filtering](docs/public/defender-cloud-apps.md), and [security information](https://github.com/CoC-MS/ALSO-Microsoft-Security-MacOS/tree/main?tab=security-ov-file). Choose and download exactly one package using the [macOS Licensing Guide](#macos-licensing-guide) bwlow : [`ALSO_MACOS_BP`](ALSO_MACOS_BP) or [`ALSO_MACOS_E5`](ALSO_MACOS_E5).
2. Follow [How to import](docs/public/how-to-import.md) for extraction and import guidance.

For controlled rollouts, we recommend using Microsoft's [deployment plans](https://learn.microsoft.com/en-us/intune/device-management/deployments/overview). This Intune feature is currently in public preview.

**Need help or have feedback?** See [Reporting issues](docs/public/reporting-issues.md) to report problems or suggest improvements.

> [!WARNING]
> All issues are public; do not include sensitive information.

### Quick navigation

| Section | What you will find |
| --- | --- |
| [Getting started](#getting-started) | Prerequisites, download, import, and staged rollout. |
| [macOS licensing guide](#macos-licensing-guide) | License compatibility and limitations. |
| [macOS configuration packages](#macos-configuration-packages) | Compare BP and E5 and review package contents. |
| [macOS coverage](#macos-coverage) | Areas covered by this repository. |
| [Notable capabilities](#notable-capabilities) | Key features and deployment considerations. |
| [Documentation](#documentation) | Links to supporting guides and the repository license. |

---

<a id="macos-licensing-guide"></a>
## macOS Licensing Guide

Choose one standalone package based on your organization's licenses and required Defender experience.

### ✅ E5 Folder (Full Experience)

The **E5 folder** is intended for organizations that have licensing for Defender for Cloud Apps.

| License | Supported |
|----------|----------|
| Microsoft 365 E7 | ✅ Full support |
| Microsoft 365 E5 | ✅ Full support |
| Microsoft 365 E3 + Defender Suite | ✅ Full support |
| Business Premium + Defender Suite | ✅ Full support |
| Microsoft 365 F3 + Defender Suite | ✅ Full support |
| Microsoft 365 F1 + Defender Suite | ✅ Full support |

The E5 package supports the Defender for Cloud Apps Cloud App Catalog workflow. Review [Defender for Cloud Apps](docs/public/defender-cloud-apps.md) and confirm your tenant's licensing and service prerequisites before deployment.

---

### ⚠️ BP Folder (Limited Experience)

The **BP folder** is designed for organizations using Microsoft 365 Business Premium and other licenses with partial feature compatibility.

| License | Supported Features |
|----------|----------|
| Microsoft 365 Business Premium | ⚠️ Supported with limitations (without full Defender for Cloud Apps experience) |
| Microsoft 365 E3 | ⚠️ Supported with limitations (without full Defender for Cloud Apps experience) |
| Microsoft 365 F3 | ⚠️ Supported with limitations (without full Defender for Cloud Apps experience) |
| Microsoft 365 F1 | ⚠️ Intune settings only. Defender settings are not supported. |

For Business Premium, the Defender starter policy uses **Custom Indicators** in Microsoft Defender rather than the Cloud App Catalog. See [Defender for Cloud Apps](docs/public/defender-cloud-apps.md) for the required service settings and limitations.

> **Important:** Microsoft 365 F1 supports deployment of Intune configuration settings only. Microsoft Defender security policy settings included in this repository are not supported with F1 licensing.

---

<a id="macos-configuration-packages"></a>
## 📦 macOS configuration packages

Each package is standalone and retains the original workload folders and exact export bytes.

| Package | Classification | JSON files |
| --- | --- | ---: |
| [`ALSO_MACOS_BP`](ALSO_MACOS_BP) | 38 BP exports + 1 Defender Custom Indicators and web content filtering readiness policy | 39 |
| [`ALSO_MACOS_E5`](ALSO_MACOS_E5) | 38 BP exports + 1 Defender for Cloud Apps Cloud App readiness policy | 39 |

> [!WARNING]
> Choose one package per tenant. Do not combine packages. Review every selected object, setting, licensing requirement, and dependency before assigning them.

<a id="macos-coverage"></a>
## 🌐 macOS coverage

| Area | Included content |
| --- | --- |
| 🛡️ Microsoft Defender for Endpoint | Automatic onboarding package that automates onboarding to Defender for Business / Endpoint plus a separate offboarding policy. |
| ☁️ Defender for Cloud Apps readiness | AV Configuration which enables Defender for Cloud Apps for E5 level tenants or Custom Indicators and Web Content filtering for Business Premium tenants |
| ✅ Compliance and Conditional Access | Compliance policies and Conditional Access policies to setup Zero trust access policies for MacBook users |
| ⚙️ Device configuration | Restriction, updates, SSO, accounts and login, FileVault and Gatekeeper settings. |
| 🌐 Microsoft Edge | Password management, profiles, updates, extensions, and security settings. |
| 📄 Microsoft 365 apps | Auto sign-in, activation, updates, service access, mapping known-folder, and backup settings. |

<a id="notable-capabilities"></a>
### ✨ Notable capabilities

- 🛡️ **Automated Defender onboarding:** The onboarding policy set and Microsoft Defender for Endpoint macOS app work together to onboard enrolled devices. Replace the sample onboarding XML with the tenant-generated file and follow [Dependencies and special handling](docs/public/dependencies-and-errors.md).
- ☁️ **Defender for Cloud Apps readiness:** The starter AV configuration supports the Cloud App Catalog workflow for appropriately licensed tenants. Business Premium uses Custom Indicators and has a more limited experience; review [Defender for Cloud Apps](docs/public/defender-cloud-apps.md).
- 🔐 **Device security and compliance:** FileVault, Firewall, Gatekeeper, device restrictions, minimum OS version, password, encryption, and system-integrity settings provide a macOS baseline.
- 🔑 **Conditional Access for macOS:** Templates cover administrators and internal users, with supporting groups and exclusion examples. Import policies in OFF mode and review assignments before enabling them.
- 🌐 **Managed Edge and Microsoft 365 apps:** Policies configure Edge security, sign-in, updates, and extensions, alongside Office activation and OneDrive access and backup settings.
- 🚪 **Controlled offboarding:** A separate Defender offboarding policy is included. Generate the offboarding XML in your tenant and review the special handling guidance before use.

---

<a id="documentation"></a>
## 📚 Documentation

| Documentation | Overview |
| --- | --- |
| 📖 [**Policy and configuration descriptions**](docs/public/policy-collections.md) | Review the descriptions of each workload collection. |
| 🚀 [**General prerequisites**](docs/public/general-prerequisites.md) | Check licensing, permissions, Defender, Intune, Conditional Access, and Apple Push certificate preparation. |
| 🍎 [**macOS prerequisites**](docs/public/macos-prerequisites.md) | Check supported device types and macOS versions. |
| 📦 [**macOS packages**](docs/public/file-structure.md) | Compare package contents and find each workload. |
| ☁️ [**Defender for Cloud Apps/Defender for Business Custom Indicators and Web Content Filtering**](docs/public/defender-cloud-apps.md) | Review starter-policy requirements and the Business Premium limitation. |
| 🧩 [**Dependencies and special handling**](docs/public/dependencies-and-errors.md) | Review Defender onboarding and offboarding requirements and limitations. |
| 📖 [**Policy naming**](docs/public/policy-naming.md) | Review the naming format and license tags. |
| 🛡️ [**Security information**](SECURITY) | Read the repository security and usage information. |
| 📜 [**License**](LICENSE) | Read the repository license. |
