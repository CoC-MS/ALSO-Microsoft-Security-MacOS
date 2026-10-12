# 🛡️ ALSO Microsoft Security MacOS Policy Templates

> A collection of Microsoft Security MacOS policy to help organizations automate onboarding/offboarding of Macbook's to/from Defender with Intune, accelerate secure deployments and implement Microsoft Security best practices with Zero trust principles.

---

> [!IMPORTANT]
> **⚠️ IMPORTANT: Read this before importing and using any policies.**

## macOS Licensing Guide

Choose one standalone package. The packages are cumulative: E5 contains every BP-compatible export plus any E5-only exports. The current repository has no E5-only exports, so both packages contain the same 39 source artifacts.

### ✅ E5 Folder (Full Experience)

Package: [`ALSO_MACOS_E5`](ALSO_MACOS_E5)

The **E5 folder** is intended for organizations that have access to the complete Microsoft Security stack used by these templates.

| License | Supported |
|----------|----------|
| Microsoft 365 E7 | ✅ Full support |
| Microsoft 365 E5 | ✅ Full support |
| Microsoft 365 E3 + Defender Suite | ✅ Full support |
| Business Premium + Defender Suite | ✅ Full support |
| Microsoft 365 F3 + Defender Suite | ✅ Full support |
| Microsoft 365 F1 + Defender Suite | ✅ Full support |

### ⚠️ BP Folder (Limited Experience)

Package: [`ALSO_MACOS_BP`](ALSO_MACOS_BP)

The **Business Premium folder** is designed for organizations using Microsoft 365 Business Premium and other licenses with partial feature compatibility.

| License | Supported Features |
|----------|----------|
| Microsoft 365 Business Premium | ⚠️ Supported with limitations (without full Defender for Cloud Apps experience) |
| Microsoft 365 E3 | ⚠️ Supported with limitations (without full Defender for Cloud Apps experience) |
| Microsoft 365 F3 | ⚠️ Supported with limitations (without full Defender for Cloud Apps experience) |
| Microsoft 365 F1 | ⚠️ Intune settings only. Defender settings are not supported. |


> **Important:** Microsoft 365 F1 supports deployment of Intune configuration settings only. Microsoft Defender security policy settings included in this repository are not supported with F1 licensing.



| Resource | Description |
| --- | --- |
| 📚 **[Documentation index](docs/public/README.md)** | Browse all deployment documentation. |
| 📖 **[Policy and configuration descriptions](docs/public/policy-collections.md)** | Review the preserved descriptions of every workload collection. |
| 🚀 **[General prerequisites](docs/public/general-prerequisites.md)** | Review roles, licensing,  prepare Intune, Defender and Apple Push certificate. |
| ☁️ **[Defender for Cloud Apps](docs/public/defender-cloud-apps.md)** | Review the exact Business Premium Custom Indicators limitation and E5 workflow. |
| 🧩 **[Dependencies and special handling](docs/public/dependencies-and-errors.md)** | Review onboarding, offboarding, Conditional Access, and tenant-specific dependencies. |
| 📖 **[Policy naming](docs/public/policy-naming.md)** | Understand licence tags and naming components. |
| 📂 **[File structure](docs/public/file-structure.md)** | Compare the two cumulative packages and workload folders. |
| 📥 **[How to import](docs/public/how-to-import.md)** | Follow the original illustrated import and post-import guidance. |
| 🐛 **[Reporting issues](docs/public/reporting-issues.md)** | Open an issue. |
| 🛡️ **[Security information](SECURITY)** | Read the security and usage information. |
| 📜 **[License](LICENSE)** | Read the repository licence. |

---

## 📦 macOS packages

Each package is standalone and retains the original workload folders and exact export bytes.

| Package | Classification | JSON files |
| --- | --- | ---: |
| [`ALSO_MACOS_BP`](ALSO_MACOS_BP) | 38 BP exports + 1 Defender for Cloud Apps starter export supported with Business Premium only when Custom Indicators are used | 39 |
| [`ALSO_MACOS_E5`](ALSO_MACOS_E5) | Cumulative: the same 39 exports; no additional E5-only source artifacts currently exist | 39 |

> [!WARNING]
> Choose **one** package per tenant. Do not combine packages. Review every selected object, setting, assignment, licence requirement, and dependency before import.

## 🌐 macOS coverage

| Area | Included content |
| --- | --- |
| Microsoft Defender for Endpoint | Automatic onboarding package that automates onboarding to Defender for Business / Endpoint plus a separate offboarding policy. |
| Defender for Cloud Apps readiness | AV Configuration which enables Defender for Cloud Apps for E5 level tenants or Custom Indicators and Web Content filtering for Business Premium tenants|
| Compliance and Conditional Access | Compliance policies and Conditional Access policies to setup Zero trust access policies for MacBook users |
| Device configuration | Restriction, updates, SSO, accounts and login, FileVault and Gatekeeper settings. |
| Microsoft Edge | Password management, profiles, updates, extensions, and security settings. |
| Microsoft 365 apps | Auto sign-in, activation, updates, service access, mapping known-folder, and backup settings. |

## 🚀 Getting started

1. Choose one package using the licensing guide above.
2. Read [General prerequisites](docs/public/general-prerequisites.md), [macOS prerequisites](docs/public/macos-prerequisites.md), [Defender for Cloud Apps](docs/public/defender-cloud-apps.md), and [Dependencies and special handling](docs/public/dependencies-and-errors.md).
3. Review the exact workload descriptions in [Policy and configuration descriptions](docs/public/policy-collections.md).
4. Follow [How to import](docs/public/how-to-import.md). **Always import Conditional Access policies in OFF mode** and use a controlled pilot.
