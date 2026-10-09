# 🛡️ ALSO Microsoft Security - macOS

> Microsoft Intune policy exports and supporting configuration for macOS, including Microsoft Defender for Endpoint onboarding and security settings.

> [!IMPORTANT]
> These exports are starting points, not ready-made tenant configurations. Review licensing, settings, tenant-specific values, dependencies, and assignments. Test in a pilot before expanding deployment, and keep a rollback plan.

| Resource | Description |
| --- | --- |
| 📂 **[Policy collections](docs/public/file-structure.md)** | Browse the exported policy sets and their contents. |
| 🚀 **[General prerequisites](docs/public/general-prerequisites.md)** | Prepare access, licensing review, and deployment readiness. |
| 🍎 **[macOS prerequisites](docs/public/macos-prerequisites.md)** | Review macOS enrollment and Defender-specific dependencies. |
| 📖 **[Policy naming](docs/public/policy-naming.md)** | Understand the naming patterns used by the exports. |
| 🏷️ **[Short-name exceptions](docs/public/short-name-exceptions.md)** | See where resource names do not follow the common pattern. |
| 📥 **[How to import](docs/public/how-to-import.md)** | Review the import workflow and special handling for selected exports. |
| 🐛 **[Reporting issues](docs/public/reporting-issues.md)** | Report problems without exposing tenant information. |
| 📜 **[License](LICENSE)** | Read the repository license. |

---

## 📦 macOS policy collections

This repository contains exported JSON resources organized by workload. It is not an application or a deployment script. Review the files and their descriptions before importing; licensing and prerequisites can differ by policy.

| Collection | Included exports |
| --- | --- |
| [MDE onboarding](ALSO_MACOS_MDE_AUTO_ONBOARDING) | 1 application, 7 Device Configuration exports, and 1 Settings Catalog export for Microsoft Defender for Endpoint onboarding. |
| [Defender Cloud Apps readiness](ALSO_MACOS_MDCA_READY) | 1 Settings Catalog export; the repository describes it as dependent on MDE onboarding. |
| [Compliance](ALSO_MACOS_COMPLIANCE_POLICIES) | 4 macOS compliance policy exports. |
| [Conditional Access](ALSO_MAC_CA_POLICIES) | 3 Conditional Access exports, 5 group exports, and a `MigrationTable.json`. |
| [Device configuration](ALSO_MACOS_DEVICE_CONFIG_POLICIES) | 6 Settings Catalog exports, including restrictions, updates, SSO, accounts and login, FileVault, and firewall/Gatekeeper settings. |
| [Microsoft Edge](ALSO_MACOS_EDGE_POLICIES) | 5 Settings Catalog exports for browser security and management. |
| [Microsoft 365 apps and OneDrive](ALSO_MACOS_OFFICE365_POLICIES) | 4 Settings Catalog exports for Office sign-in, app updates, and OneDrive. |
| [MDE offboarding](ALSO_MACOS_MDE_AUTO_OFFBOARDING) | 1 Device Configuration export for offboarding. |

The counts above describe the JSON files currently in each collection; they are not a recommendation to import or assign everything together. See [Policy collections](docs/public/file-structure.md) for details.

## 🌐 macOS coverage

| Area | Included content |
| --- | --- |
| 🛡️ **Defender for Endpoint** | An onboarding collection with the macOS Defender application export and related device configuration, plus a separate offboarding export. |
| ✅ **Compliance and access** | macOS compliance policies and Conditional Access exports with associated group resources. |
| 🔒 **Device security** | Settings for FileVault, firewall/Gatekeeper, restrictions, accounts and login, updates, and SSO. |
| ☁️ **Defender for Cloud Apps readiness** | A separate antivirus configuration export described as requiring MDE onboarding first; service and licensing prerequisites must be checked independently. |
| 🌐 **Browser and productivity** | Microsoft Edge, Microsoft 365 app, and OneDrive settings. |

## ✨ Deployment considerations

- **Onboarding is a set:** Review and deploy the application and related policies as described in [macOS prerequisites](docs/public/macos-prerequisites.md). The tenant-specific onboarding package and service connections must be prepared separately.
- **Conditional Access is high impact:** Import Conditional Access exports in **Off** mode, review their conditions, assignments, exclusions, and group dependencies, then test before enabling.
- **Offboarding needs tenant-specific content:** The repository README directs administrators to download a macOS MDM offboarding package from the Defender portal and use it with the offboarding policy.
- **Names are not licensing advice:** Values such as `BP`, `BPE5`, impact labels, or assignment suffixes are part of exported names. Verify requirements for each resource in Microsoft documentation and in the target tenant.

---

## 🚀 Getting started

1. ✅ Read [General prerequisites](docs/public/general-prerequisites.md) and [macOS prerequisites](docs/public/macos-prerequisites.md).
2. 📂 Choose and inspect the relevant collection using [Policy collections](docs/public/file-structure.md).
3. 📖 Review names, settings, descriptions, licensing, and assignment scope.
4. 📥 Follow [How to import](docs/public/how-to-import.md), then validate the result in a test group before wider deployment.
