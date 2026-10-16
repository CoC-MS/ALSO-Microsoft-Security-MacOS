# 🧩 Dependencies and special handling

[Documentation index](README.md)

## Before using ALSO_MACOS_MDE_AUTO_ONBOARDING

1. Sign in to security.microsoft.com with Security Administrator role
2. Navigate to Settings-> Endpoint -> Onboarding

Direct access link: https://security.microsoft.com/securitysettings/endpoints/onboarding 

3. Choose MacOS -> MDM
4. Download onboarding xml file and upload it to your onboarding policy in Intune (Intune Administrator role required)
5. Replace the `.xml` file inside the policy **ALSO – LI – BP – Basic – v1.0– MacOS – Device Configuration - MDE Auto Onboarding - D** with the downloaded one.

<img width="1532" height="950" alt="image" src="https://github.com/user-attachments/assets/3826eb7f-522a-4eb3-a212-afc183060ecb" />

<img width="1109" height="1233" alt="image" src="https://github.com/user-attachments/assets/8d35575d-4d76-4bbb-a54f-2810d7e1b177" />

6. -Assign policies in Devices -> MacOS -> Configuration
   - Assign all policies to your security **Device Group for MacOS devices** or **All Devices**

<img width="1118" height="1177" alt="image" src="https://github.com/user-attachments/assets/12a4476a-f66d-4d32-a000-3780d310494a" />

<img width="1152" height="292" alt="image" src="https://github.com/user-attachments/assets/6378831d-c626-4eb5-9ecd-8cd163cdf763" />

7.  Set Defender MacOS app as required in Apps-> MacOs
    - Microsoft Defender for Endpoint (macOS app) must be assigned as **Required** to the same **Device Group** / **All Devices**.

<img width="1593" height="866" alt="image" src="https://github.com/user-attachments/assets/bd921b3a-ffa3-46d2-b164-e6732d553ac0" />

8. Test onboarding by enrolling your test device(s) to Intune
    - On a macOS device, go to [aka.ms/enrollmymac](https://aka.ms/enrollmymac)
    - The Mac should be automatically enrolled into Defender for Endpoint **after device enrollment** without any manual steps.

<img width="1883" height="1247" alt="image" src="https://github.com/user-attachments/assets/574837ed-c9ec-41b7-bae7-26025698cee2" />


# Before using ALSO_MACOS_MDE_AUTO_OFFBOARDING

1. Sign in to security.microsoft.com with Security Administrator role
2. Navigate to Settings-> Endpoint -> Offboarding
3. Choose MacOS -> MDM
4. Download offboarding xml file and upload it to your offboarding policy in Intune (Intune Administrator role required)
5. Assign to device or device group

Direct access link: https://security.microsoft.com/securitysettings/endpoints/offboarding 

<img width="2306" height="1303" alt="image" src="https://github.com/user-attachments/assets/5151ba3e-f0a3-42d4-ad5b-a595bcc5a6f4" />

The offboarding XML is tenant-generated and is not a separate source artifact in this repository.
