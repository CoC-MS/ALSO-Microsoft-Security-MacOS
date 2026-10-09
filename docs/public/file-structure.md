# 📂 Policy collections

[Documentation index](README.md)

This repository contains pre-generated Intune JSON exports organized into workload folders at the repository root. These folders are collections, not cumulative licence packages. The folders do not include a shared deployment tool or a documented package manifest.

## 📦 Collections

| Folder | Contents |
| --- | --- |
| [`ALSO_MACOS_MDE_AUTO_ONBOARDING`](../../ALSO_MACOS_MDE_AUTO_ONBOARDING) | 1 macOS app export, 7 Device Configuration exports, and 1 Settings Catalog export. |
| [`ALSO_MACOS_MDCA_READY`](../../ALSO_MACOS_MDCA_READY) | 1 Settings Catalog export for Defender Antivirus configuration. |
| [`ALSO_MACOS_COMPLIANCE_POLICIES`](../../ALSO_MACOS_COMPLIANCE_POLICIES) | 4 compliance policy exports. |
| [`ALSO_MAC_CA_POLICIES`](../../ALSO_MAC_CA_POLICIES) | 3 Conditional Access exports, 5 group exports, and `MigrationTable.json`. |
| [`ALSO_MACOS_DEVICE_CONFIG_POLICIES`](../../ALSO_MACOS_DEVICE_CONFIG_POLICIES) | 6 Settings Catalog exports for macOS device configuration. |
| [`ALSO_MACOS_EDGE_POLICIES`](../../ALSO_MACOS_EDGE_POLICIES) | 5 Settings Catalog exports for Microsoft Edge. |
| [`ALSO_MACOS_OFFICE365_POLICIES`](../../ALSO_MACOS_OFFICE365_POLICIES) | 4 Settings Catalog exports for Microsoft 365 apps and OneDrive. |
| [`ALSO_MACOS_MDE_AUTO_OFFBOARDING`](../../ALSO_MACOS_MDE_AUTO_OFFBOARDING) | 1 Device Configuration export for MDE offboarding. |

The counts reflect the JSON files currently checked into each folder. They do not describe licensing, deployment order, or whether all resources should be assigned together. Inspect each export and its description in Intune before use.

## 🗂️ Export types and dependencies

- The onboarding collection includes an application, Device Configuration exports, and a Settings Catalog export. Follow [macOS prerequisites](macos-prerequisites.md) and inspect each resource's description; tenant-specific onboarding content is not a substitute for enabling the required tenant services.
- The Defender Cloud Apps readiness collection contains one Settings Catalog export. Its description says to deploy the MDE onboarding policies first. Review the applicable Defender service and licensing requirements before use.
- The Conditional Access folder contains distinct policy, group, and migration-table JSON files. `MigrationTable.json` is import metadata, not a policy. Import Conditional Access policies in **Off** mode and review group references and assignments before enabling them.
- The offboarding folder contains a JSON export. The repository README says to obtain the macOS MDM offboarding package from the Defender portal for use with that policy; that tenant-specific package is not a separate checked-in file.

There are no Windows package folders, build manifests, or policy deployment scripts in the current macOS repository. For import guidance, see [How to import](how-to-import.md).
