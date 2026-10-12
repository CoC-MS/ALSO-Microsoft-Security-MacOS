# 🧩 Dependencies and special handling

[Documentation index](README.md)

## Microsoft Defender for Endpoint onboarding dependency

> [!IMPORTANT]
> All of these policy templates and the application are required to enable seamless automatic onboarding of macOS devices to Microsoft Defender for Endpoint when they are enrolled in Intune.

## Defender for Cloud Apps starter dependency

> [!IMPORTANT]
> ALSO_MACOS_MDE_AUTO_ONBOARDING must be imported and assigned to the target device group before deploying any other policies in this package.
> This policy will also work with Microsoft 365 Business Premium, but it uses Custom Indicators in Microsoft Defender rather than the cloud app catalog available through Microsoft Defender for Cloud Apps.

See [Defender for Cloud Apps](defender-cloud-apps.md) for the complete original Business Premium and E5 portal guidance. All other Defender for Cloud Apps policies cannot be used with Business Premium and belong only in `ALSO_MACOS_E5`; none are present in the current source artifacts.

## Conditional Access

> [!IMPORTANT]
> **Always import Conditional Access policies in OFF mode**:

Ensure you have Conditional Access Administrator role before importing Conditional Access policies.

The `ALSO_MAC_CA_POLICIES` workload contains three Conditional Access policy templates, five group templates, and `MigrationTable.json`. Keep these files together in the chosen package and review group references, exclusions, assignments, and migration mappings before enabling any policy.

## Before using ALSO_MACOS_MDE_AUTO_OFFBOARDING

1. Sign in to security.microsoft.com with Security Administrator role
2. Navigate to Settings-> Endpoint -> Offboarding
3. Choose MacOS -> MDM
4. Download offboarding xml file and upload it to your offboarding policy in Intune
5. Assign to device or device group

<img width="2306" height="1303" alt="image" src="https://github.com/user-attachments/assets/5151ba3e-f0a3-42d4-ad5b-a595bcc5a6f4" />

The offboarding XML is tenant-generated and is not a separate source artifact in this repository.
