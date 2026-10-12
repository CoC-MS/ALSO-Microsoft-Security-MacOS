# 📥 How to import

[Documentation index](README.md)

## How to import ALSO_MACOS_MDE_AUTO_ONBOARDING AND OTHER POLICY TEMPLATES?

> [!IMPORTANT]
> **Always import Conditional Access policies in OFF mode**:
> Ensure you have Conditional Access Administrator role before importing Conditional Access policies.

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

8. Download hole project and unzip

<img width="401" height="373" alt="image" src="https://github.com/user-attachments/assets/99f1e353-44f6-4bd5-85d7-0c2af71925f3" />

9. Choose Bulk-> Import and find right folder

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

1. As with Step 2 above, review the configuration to ensure it meets your requirements, then assign the policies to the appropriate device group(s) or to All Devices.
