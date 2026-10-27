# 📖 Policy and configuration descriptions

[Documentation index](README.md)

## What's included in ALSO_MACOS_MDE_AUTO_ONBOARDING

This policy set is designed to automate the onboarding of macOS devices to Microsoft Defender for Business and Microsoft Defender for Endpoint for both personally owned and corporate-owned devices.

This folder contains:

| Component | Description |
|-----------|-------------|
| Application | 1 Application: Microsoft Defender for Endpoint for MacOS |
| Settings Catalog Policies | 1 policy template: MDE System Extension Settings |
| Device Configuration Policies | 7 policy templates: MDE Accessibility Settings, MDE Auto-Onboarding Settings, MDE Background Services Settings, MDE Full Disk Access Settings, MDE Notification Settings, and MDE Network filter settings|

> [!IMPORTANT]
> All of these policy templates and the application are required to enable seamless automatic onboarding of macOS devices to Microsoft Defender for Endpoint when they are enrolled in Intune.

## What's included in ALSO_MACOS_MDCA_READY/SettingsCatalog

This policy is designed to help organizations get started with Microsoft Defender for Cloud Apps cloud app blocking and monitoring. It includes the required Real-Time Protection, Network Protection, and Cloud Protection settings, reducing the need for manual configuration.

This folder contains:

| Component | Description |
|-----------|-------------|
| Settings Catalog Policies | 1 policy template:  AV Configuration |

> [!IMPORTANT]
> ALSO_MACOS_MDE_AUTO_ONBOARDING must be imported and assigned to the target device group before deploying any other policies in this package.
> This policy will also work with Microsoft 365 Business Premium, but it uses Custom Indicators in Microsoft Defender rather than the cloud app catalog available through Microsoft Defender for Cloud Apps.

The Business Premium exception above applies only to this one starter policy. All other Defender for Cloud Apps policies require E5/Defender Suite licensing and belong only in `ALSO_MACOS_E5`; the current source repository contains no additional Defender for Cloud Apps policies.

## What's included in ALSO_MACOS_COMPLIANCE_POLICIES/CompliancePolicies

This policy set is designed to establish a baseline level of device compliance for use with Conditional Access policies that require compliant devices. Ready-to-use Conditional Access policy templates are available in the next section to simplify deployment.

This approach aligns with Microsoft's Zero Trust principles by helping ensure that only compliant and trusted devices can access organizational resources.

This folder contains:

| Component | Description |
|-----------|-------------|
| Compliance Policies | 4 policy template:  Disk Encryption, Firewall, Password and OS requirements, App download sources, System integrity etc. |

## What's included in ALSO_MACOS_CA_POLICIES

Includes Conditional Access policiy templates for internal users and administrators that require devices to be compliant in Microsoft Intune and enrolled when signing in from macOS devices.

This approach aligns with Microsoft's Zero Trust principles by ensuring that access is granted only from trusted, compliant, and managed devices.

| Component | Description |
|-----------|-------------|
| Compliance Policies | 3 policy template:  Requiring compliant device check. |
| Security groups | 3 security groups:  For exclusions in Conditional Access policies. |
| MigrationTable.json | For import job |

> [!IMPORTANT]
> **Always import Conditional Access policies in OFF mode**:

## What's included in ALSO_MACOS_DEVICECONFIG_POLICIES

Includes policies for FileVault, Gatekeeper, software updates, account and sign-in security, and general device restrictions, providing a secure baseline configuration for MacBooks.

| Component | Description |
|-----------|-------------|
| SettingsCatalog | 6 policy template |

## What's included in ALSO_MACOS_EDGE_POLICIES

Includes policies for password management, profile and synchronization settings, browser updates, extension controls, and security hardening, providing a baseline security configuration for Microsoft Edge on MacBooks.

| Component | Description |
|-----------|-------------|
| SettingsCatalog | 5 policy template |

## What's included in ALSO_MACOS_OFFICE365_POLICIES

Includes policies for Microsoft 365 Apps, including automatic sign-in and activation, OneDrive backup and folder synchronization, update policies, and access controls to provide baseline security and an optimized end-user experience.

| Component | Description |
|-----------|-------------|
| SettingsCatalog | 4 policy template |

## What's included in ALSO_MACOS_MDE_AUTO_OFFBOARDING

Includes a policy and sample XML file for automating the offboarding of MacBook devices from Defender for Business and Defender for Endpoint. Please review the documentation before use.

| Component | Description |
|-----------|-------------|
| DeviceConfiguration | 1 policy template with sammple xml file |

**Disclaimer:** Licensing prerequisites and feature availability listed on this page may be incorrect, incomplete, or outdated. We strongly recommend verifying all licensing information against the latest official Microsoft licensing documentation before making any purchasing or deployment decisions.

**Enterprise licenses:** [Microsoft Enterprise Plan Comparison](https://cdn-dynmedia-1.microsoft.com/is/content/microsoftcorp/microsoft/bade/documents/products-and-services/en-us/education/Modern-Work-Plan-Comparison-Enterprise.pdf)

**SMB licenses:** [Microsoft SMB Plan Comparison](https://cdn-dynmedia-1.microsoft.com/is/content/microsoftcorp/microsoft/bade/documents/products-and-services/en-us/education/Modern-Work-Plan-Comparison-SMB.pdf)
