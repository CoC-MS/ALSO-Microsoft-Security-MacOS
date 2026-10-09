# 🍎 macOS prerequisites

[Documentation index](README.md)

Review the relevant steps for the collection you intend to deploy. Portal names and product requirements can change; verify them in the target tenant and in current Microsoft documentation.

## 🛡️ Microsoft Defender for Endpoint onboarding

The repository's onboarding guidance identifies Security Administrator and Intune Administrator roles for its setup steps. Before deploying the onboarding collection:

1. Confirm that Microsoft Defender for Endpoint or Defender for Business is available and set up in the tenant.
2. In the Defender portal, confirm the Microsoft Intune connection is enabled.
3. In the Intune admin center, confirm the Defender connection status is enabled.
4. Confirm the Apple MDM Push Certificate is active for macOS enrollment.
5. Check the supported macOS versions and device-enrollment requirements in Microsoft's current documentation.
6. Obtain the onboarding package for the target tenant from the Defender portal and follow Microsoft's current Intune onboarding instructions. Review the exported MDE Auto Onboarding resource and replace or configure any tenant-specific onboarding content as required; do not import sample values unchanged.

The repository describes the onboarding collection as a coordinated set of the Microsoft Defender for Endpoint app and related configuration exports. Inspect every resource description and assign the app and policies only to the intended pilot devices.

## ☁️ Defender for Cloud Apps readiness

The `ALSO_MACOS_MDCA_READY` collection contains one antivirus configuration export. Its description says to deploy the MDE onboarding policies first and refers to Defender for Cloud Apps blocking and monitoring capabilities.

The repository's existing setup guidance distinguishes Business Premium use of custom network indicators from tenants using Defender for Cloud Apps features. Confirm the exact product entitlement and current Defender portal settings that apply to your tenant before enabling either workflow. The JSON export alone does not provision a Defender for Cloud Apps service or establish licensing.

## 🔄 MDE offboarding

The repository README directs administrators to sign in to the Defender portal, download the macOS **MDM** offboarding package, and use it with the offboarding policy. The tenant-generated package is not a separate checked-in file. Verify the target device scope and intended effect before assigning an offboarding policy.

## 📚 Microsoft sources

- [Microsoft Defender for Endpoint on macOS](https://learn.microsoft.com/en-us/defender-endpoint/microsoft-defender-endpoint-mac) — platform requirements and product guidance.
- [Microsoft Intune macOS enrollment](https://learn.microsoft.com/en-us/intune/intune-service/enrollment/macos-enroll) — enrollment options and preparation.
- [Apple MDM Push Certificate](https://learn.microsoft.com/en-us/intune/device-enrollment/apple/create-mdm-push-certificate) — certificate setup and renewal.
- [Deploy Microsoft Defender for Endpoint on macOS with Intune](https://learn.microsoft.com/en-us/defender-endpoint/mac-install-with-intune) — deployment, onboarding, and verification guidance.
