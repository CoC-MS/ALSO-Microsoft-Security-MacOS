# 🚀 General prerequisites

[Documentation index](README.md)

> [!IMPORTANT]
> **⚠️ IMPORTANT: Read this before importing and using any policies.**

Choose either [`ALSO_MACOS_BP`](../../ALSO_MACOS_BP) or [`ALSO_MACOS_E5`](../../ALSO_MACOS_E5) using the [macOS Licensing Guide](../../README.md#macos-licensing-guide). Review each policy, licence requirement and settings before import.

**Required administrator roles to do these steps**

Security Administrator and Intune Administrator roles

For Conditional Access:

At least Conditional Access Administrator role assigned

> [!IMPORTANT]
> **Always import Conditional Access policies in OFF mode**:
> Ensure you have Conditional Access Administrator role before importing Conditional Access policies.


**Device types supported**
   - Works with both **personally-owned devices (work profile)** and **corporate-owned devices**

**Supported MacOS versions**

Per September 2026:

27 (Golden Gate), 26 (Tahoe), 15 (Sequoia)

Reference: Microsoft Learn

Always double check here as well: https://learn.microsoft.com/nb-no/defender-endpoint/microsoft-defender-endpoint-mac-prerequisites#system-requirements

1. **Verify Defender for Business/Endpoint availability**
   - Go to [security.microsoft.com](https://security.microsoft.com)
   - Navigate to **Assets → Devices** and ensure your Defender for Business / Defender for Endpoint instance is set up in the tenant.

<img width="1435" height="660" alt="image" src="https://github.com/user-attachments/assets/d4cd25aa-b369-4046-9fec-7af049784305" />

2. **Enable Intune connection in Defender portal**
   - Go to **System → Settings → Endpoints**
   - Ensure that the **Microsoft Intune connection** is turned **ON**.

<img width="1846" height="996" alt="image" src="https://github.com/user-attachments/assets/020b15de-161a-4662-b787-e7a5ea2174f2" />

3. **Confirm Defender connection in Intune admin center**
   - Go to [intune.microsoft.com](https://intune.microsoft.com)
   - Navigate to **Endpoint Security → Microsoft Defender for Endpoint**
   - Ensure the **Connection status** is **Enabled**.

<img width="1030" height="353" alt="image" src="https://github.com/user-attachments/assets/4622ac18-83ec-47cf-9e15-92c883d00981" />

4. **Set up Apple MDM Push Certificate**
   - In the Intune admin center, go to **Devices → macOS → Enrollment**
   - Ensure the **Apple MDM Push Certificate** is active.

<img width="1529" height="695" alt="image" src="https://github.com/user-attachments/assets/e48aa0c6-5b64-4157-a8df-a6ac80db084f" />
