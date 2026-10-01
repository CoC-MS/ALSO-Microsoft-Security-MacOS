# 🛡️ ALSO Microsoft Security MacOS Policy Templates

> A collection of Microsoft Security MacOS policy to help organizations automate onboarding/offboarding of Macbook's to/from Defender with Intune, accelerate secure deployments and implement Microsoft Security best practices with Zero trust principles.

**Works with Business Premium and up.**

---


> [!IMPORTANT]
> **⚠️ IMPORTANT: Read this before importing and using any policies.**  

| Resource | Description |
|-----------|-------------|
| 🛡️ **Security Information** | [View Security Policy](https://github.com/CoC-MS/ALSO-Microsoft-Security-MacOS/tree/main?tab=security-ov-file) |
| 📖 **ALSO_MACOS_MDE_AUTO_ONBOARDING Description** | [View ALSO_MACOS_MDE_AUTO_ONBOARDING description](https://github.com/CoC-MS/ALSO-Microsoft-Security-MacOS/tree/main?tab=readme-ov-file#before-importing-also_macos_mde_auto_onboarding) |
| 📖 **ALSO_MACOS_MDCA_READY Description** | [View ALSO_MACOS_MDCA_READY description](https://github.com/CoC-MS/ALSO-Microsoft-Security-MacOS/blob/main/README.md#whats-included-in-also_macos_mdca_readysettingscatalog) |
| 📖 **ALSO_MACOS_ALSO_MACOS_COMPLIANCE_POLICIES Description** | [View ALSO_MACOS_MDCA_READY description](https://github.com/CoC-MS/ALSO-Microsoft-Security-MacOS/tree/main#whats-included-in-also_macos_compliance_policiescompliancepolicies) |
| 📖 **ALSO_MACOS_ALSO_MACOS_CA_POLICIES Description** | [View ALSO_MACOS_MDCA_READY description](https://github.com/CoC-MS/ALSO-Microsoft-Security-MacOS/blob/main/README.md#whats-included-in-also_macos_ca_policies) |
| 🚀 **Before Importing MACOS_MDE_AUTO_ONBOARDING** | [Read Before Importing Policies](https://github.com/CoC-MS/ALSO-Microsoft-Security-MacOS/tree/main?tab=readme-ov-file#before-importing-also_macos_mde_auto_onboarding) |
| 🚀 **Before Using MACOS_MDCA_READY** | [Read Before Using Policies](https://github.com/CoC-MS/ALSO-Microsoft-Security-MacOS/blob/main/README.md#before-using-also_macos_mdca_ready-with-business-premium-or-defender-suite-or-microsoft-365-e5) |

---

## 📂 File Structure

All files are organized into categories

```text
/
├── ALSO_MACOS_MDE_AUTO_ONBOARDING/
├── Applications 1 application
├── DeviceConfiguration 8 Device Configuration policy templates
├── SettingsCatalog 1 SettingsCatalog policy template

├── ALSO_MACOS_MDCA_READY/SettingsCatalog
1 policy template

├── ALSO_MACOS_CIMPLIANCE_POLICIES/CompliancePolicies
├── 4 policy templates

├── ALSO_MACOS_CA_POLICIES/
├── Conditional Access 3 policy templates
├── Groups 5 group templates
├── MigrationTable.json

├── ALSO_MACOS_DEVICE_CONFIG_POLICIES/SettingsCatalog
6 policy templates

├── ALSO_MACOS_EDGE_POLICIES/SettingsCatalog
5 policy templates

├──ALSO_MACOS_OFFICE365_POLICIES/SettingsCatalog
4 policy templates 



```

### License Tag Description

| Tag | Minimum Required License |
|:---:|--------------------------|
| **BP** | Microsoft 365 Business Premium or Intune Plan 1 + Defender for Business |
| **E5** | Microsoft Defender Suite (for Business Premium, Microsoft 365 E3, or Microsoft 365 E5) |
| **A365** | Agent 365 Standalone license combined with Microsoft Defender Suite for Business Premium, Microsoft 365 E3/E5, or Microsoft 365 E7 |

---

## 📖 Naming Convention

All policy templates follow the naming format below:

```text
<ALSO>-<ImpactLevel>-<MinimumLicense>-<BaselineLevel>-<Version>-<OS>-<Main Category>-<Sub Category>-<Settings>-<Assignment>
```

### Example

```text
ALSO – LI – BP – Basic – v1.0– MacOS – Device Configuration - MDE System Extensions - D
```

---

## 🧩 Naming Components

| Component | Description |
|-----------|-------------|
| **ALSO** | Company providing the policy template to have a better control |
| **Impact** | Impact level of policy, low (LI), medium (MI) or high (HI) |
| **MinimumLicense** | Minimum Microsoft license required to use the policy |
| **BaselineLevel** | Baseline level of policy, Basic, Advanced |
| **Version** | Policy version, v1.0, v1.1 etc|
| **MacOS** | Operating system |
| **MainCategory** | Name of main category, Device Configuration, Device Compliance etc|
| **SubCategory** | Name of sub category, MDE, AV, Disk etc|
| **Settings** | Short settings description |
| **Assignment** | Assignment scope- device (D) or user (U)|


---

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

## What's included in ALSO_MACOS_DEVICECONFIG_POLICIES

Includes policies for FileVault, Gatekeeper, software updates, account and sign-in security, and general device restrictions, providing a secure baseline configuration for MacBooks.

| Component | Description |
|-----------|-------------|
| SettingsCatalog | 6 policy template:  Requiring compliant device check. |

## What's included in ALSO_MACOS_EDGE_POLICIES

Includes policies for password management, profile and synchronization settings, browser updates, extension controls, and security hardening, providing a baseline security configuration for Microsoft Edge on MacBooks.

| Component | Description |
|-----------|-------------|
| SettingsCatalog | 5 policy template:  Requiring compliant device check. |

## What's included in ALSO_MACOS_OFFICE365_POLICIES

Includes policies for Microsoft 365 Apps, including automatic sign-in and activation, OneDrive backup and folder synchronization, update policies, and access controls to provide baseline security and an optimized end-user experience.

| Component | Description |
|-----------|-------------|
| SettingsCatalog | 4 policy template:  Requiring compliant device check. |

---

## Before importing (ALSO_MACOS_MDE_AUTO_ONBOARDING) 

> [!IMPORTANT]
> **PLEASE ENSURE THAT YOU HAVE COMPLETED THESE STEPS, BEFORE YOU START IMPORTING**:

**Required administrator roles to do these steps**

Security Administrator and Intune Administrator roles

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


## Before using ALSO_MACOS_MDCA_READY with Business Premium or Defender Suite, Purview Suite or Microsoft 365 E5 

> [!IMPORTANT]
> **PLEASE ENSURE THAT YOU HAVE COMPLETED THESE STEPS, BEFORE YOU START USING THIS POLICY**:

**Required administrator roles to do these steps**

Security Administrator 

**Device types supported** 
   - Works with both **personally-owned devices (work profile)** and **corporate-owned devices**

**Supported MacOS versions**

Per September 2026:

27 (Golden Gate), 26 (Tahoe), 15 (Sequoia)

Reference: Microsoft Learn

1. Navigate to security.microsoft.com -> Settings -> Cloud Apps

<img width="1513" height="1165" alt="image" src="https://github.com/user-attachments/assets/fc9c923d-144c-42c1-a900-5b193c56908e" />

**For Microsoft 365 Business Premium** users 

1. Navigate to security.microsoft.com -> Settings -> Endpoints -> Optional features (first page)
2. Toggle on Custom network indicators and Save
<img width="1599" height="1221" alt="image" src="https://github.com/user-attachments/assets/f472d1d9-41f3-4b33-bf97-2eb77d24f2c5" />

3. You can now add your IP's , URL's etc manually if you wish to block or monitor those websites after your policy have been pushed out to your Mac devices.

**For Defender Suite, Purview Suite or Microsoft 365 E5**  users 

1. Navigate to security.microsoft.com -> Settings -> Cloud Apps

<img width="1513" height="1165" alt="image" src="https://github.com/user-attachments/assets/fc9c923d-144c-42c1-a900-5b193c56908e" />

2. Ensure you check "Enforce App Access" and Save.

<img width="1429" height="949" alt="image" src="https://github.com/user-attachments/assets/4f324487-6b4a-476a-9f3b-5629d57a1331" />

3. Navigate to Endpoint section in settings and toggle this one ON (Microsoft Defender For Cloud Apps and Save


<img width="1607" height="1224" alt="image" src="https://github.com/user-attachments/assets/f34133fb-1356-4b2a-9133-ac2f693271f6" />

4. You can now block and monitor apps for Cloud Apps -> Cloud Apps catalog section after your policy have been pushed out to your Mac devices. 

## How to import policy templates (ALSO_MACOS_MDE_AUTO_ONBOARDING) to automate onboarding of MacOS to Defender for Business and Endpoint

1. Download Micke M Intune Management Tool from here:  https://github.com/Micke-K/IntuneManagement
2. Extract folder and Start with start.cmd in the folder (works without local administrator rights on Windows and MacOS)
   
   <img width="635" height="247" alt="image" src="https://github.com/user-attachments/assets/ae7405c2-17cb-43a1-a96e-cd60181a2619" />

4. Command window and UI will open
5. Press on icon in upper right corner to sign in

   <img width="1311" height="965" alt="image" src="https://github.com/user-attachments/assets/2e835f79-5e07-4c7d-bd7c-5bd4976fde50" />

6. You may need a Global Administrator to consent to required API permissions first time if have not used these tool before. This can be done after sign-in by pressing same icon in upper right corner once more and press "Request Consent". Command Graph Command Line Tools application will be registered in Entra. Feel free to remove it after import or remove at least admin consent.

   <img width="294" height="145" alt="image" src="https://github.com/user-attachments/assets/675ebdc9-dc87-4633-bfa5-fbb92f7ba53d" />


7. After sign in and admin consent navigate to Bulk button in the left upper corner and press Import

   <img width="273" height="202" alt="image" src="https://github.com/user-attachments/assets/9e8b32ce-93fe-4ef8-9c19-325d138add8c" />

8. Download ALSO_MACOS_MDE_AUTO_ONBOARDING.zip from this repo https://github.com/CoC-MS/ALSO-Microsoft-Security-MacOS/blob/main/ALSO_MACOS_MDE_AUTO_ONBOARDING.zip, find and extract folder and choose ALSO_MACOS_MDE_AUTO_ONBOARDING folder.
9. Choose Bulk-> Import and find extracted folder
   
   <img width="391" height="411" alt="image" src="https://github.com/user-attachments/assets/e03b2025-83fd-45c0-9122-25f29fbb3e69" />
   
10. Check "Add Object name to path" and Press Import

   <img width="2256" height="861" alt="image" src="https://github.com/user-attachments/assets/ec182c21-9982-4f57-ae03-07022f66fbff" />

   

 ## After importing ALSO_MACOS_MDE_AUTO_ONBOARDING 

1. - Download your macOS onboarding package from the Defender portal. Follow the instructions in the policy description.
   - Replace the `.xml` file inside the policy **ALSO – LI – BP – Basic – v1.0– MacOS – Device Configuration - MDE Auto Onboarding - D** with the downloaded one.

<img width="1532" height="950" alt="image" src="https://github.com/user-attachments/assets/3826eb7f-522a-4eb3-a212-afc183060ecb" />

<img width="1109" height="1233" alt="image" src="https://github.com/user-attachments/assets/8d35575d-4d76-4bbb-a54f-2810d7e1b177" />

2. -Assign policies in Devices -> MacOS -> Configuration
   - Assign all policies to your security **Device Group for MacOS devices** or **All Devices**
     
<img width="1118" height="1177" alt="image" src="https://github.com/user-attachments/assets/12a4476a-f66d-4d32-a000-3780d310494a" />

<img width="1152" height="292" alt="image" src="https://github.com/user-attachments/assets/6378831d-c626-4eb5-9ecd-8cd163cdf763" />

     
3.  Set Defender MacOS app as required in Apps-> MacOs
    - Microsoft Defender for Endpoint (macOS app) must be assigned as **Required** to the same **Device Group** / **All Devices**.

<img width="1593" height="866" alt="image" src="https://github.com/user-attachments/assets/bd921b3a-ffa3-46d2-b164-e6732d553ac0" />


4. Test onboarding by enrolling your test device(s) to Intune
    - On a macOS device, go to [aka.ms/enrollmymac](https://aka.ms/enrollmymac)  
    - The Mac should be automatically enrolled into Defender for Endpoint **after device enrollment** without any manual steps.


 ## After importing all other packages
 1. Same as above on step 2, you need to check configuration if it fits your needs and assign to device group(s) or All Devices. 


