# 🚀 General prerequisites

[Documentation index](README.md)

Review these items before importing macOS resources into Microsoft Intune.

> [!IMPORTANT]
> A collection name or policy name does not confirm that the required license, service, permissions, or assignments are in place. Verify requirements for every resource you plan to use.

---

## 🔐 Licensing and access

The exported names include labels such as `BP` and `BPE5`, but those labels are not a substitute for checking the current Microsoft product terms, service availability, and requirements of the individual policy settings. In particular, verify Defender for Endpoint and Defender for Cloud Apps entitlements before using related features.

Use accounts with the Intune permissions needed to import and manage the selected resources. The repository's onboarding instructions call for Security Administrator and Intune Administrator roles for the listed setup steps. Its Conditional Access instructions call for Conditional Access Administrator before importing those policies. Confirm the least-privilege roles and approvals for your tenant.

## 🧰 Review and dependencies

Before import:

- Inspect the exported settings, descriptions, references, names, and intended device or user scope.
- Identify tenant-specific values, groups, exclusions, assignments, and service connections.
- Check dependencies between collections; the Defender Cloud Apps readiness export says MDE onboarding policies must be deployed first.
- Obtain tenant-generated onboarding or offboarding content where required. Do not reuse another tenant's package or assume the repository contains a ready-to-use package.
- Plan how to verify policy status and user impact, and how to roll back or recover if the deployment does not behave as intended.

## 🍎 Enrollment and deployment readiness

Confirm that macOS devices can be enrolled and managed in the intended Intune tenant, including an active Apple MDM Push Certificate where required. Check Microsoft's current macOS system requirements and enrollment guidance for the devices and management method you use.

Start with a test device or pilot group. Review scope carefully, especially for Conditional Access, compliance, FileVault, firewall, and account settings. Expand deployment only after validating the expected outcome.

See [macOS prerequisites](macos-prerequisites.md) for Defender-specific setup and [How to import](how-to-import.md) for the import workflow.

## 📚 Microsoft sources

- [Microsoft Intune licensing](https://learn.microsoft.com/en-us/intune/intune-service/fundamentals/licenses) — confirm product and service entitlements.
- [Apple MDM Push Certificate](https://learn.microsoft.com/en-us/intune/device-enrollment/apple/create-mdm-push-certificate) — certificate setup and renewal.
- [Microsoft Defender for Endpoint on macOS](https://learn.microsoft.com/en-us/defender-endpoint/microsoft-defender-endpoint-mac) — current platform and product guidance.
