##### As a cybersecurity, ensuring the Windows have a latest update and patch management is one of the best practices in making sure that our system is always protected against known vulnerabilities.

## 🧩 1. Enable Windows Update for Automatic Updates
* We should make sure that Windows automatically downloads and installs updates to keep our system secure.
  
## Steps for Enabling Automatic Updates

#### Open Windows Update Settings
* Press Win + I → **Windows Update** (on Windows 11)
* Click **"Advanced options"**

<img width="995" height="645" alt="Screenshot 2025-11-11 at 16 41 30" src="https://github.com/user-attachments/assets/e744156c-a617-4b90-a7cd-1c0b9039256d" />

* Turn on **“Receive updates for other Microsoft products”** and **“Notify me when a restart is required to finish updating.”**
  
<img width="995" height="614" alt="Screenshot 2025-11-11 at 16 41 48" src="https://github.com/user-attachments/assets/1bc401cd-2388-4a0b-ab5f-350510f33d51" />

* Make sure to set up the active hours to avoid interuptions during working hours. 

<img width="995" height="614" alt="Screenshot 2025-11-11 at 16 42 47" src="https://github.com/user-attachments/assets/f2a19c3f-19e6-46d1-bf96-af3096c38444" />

* Run this command to verify the changes: **_Get-ItemProperty -Path "HKLM:\SOFTWARE\Microsoft\WindowsUpdate\UX\Settings"_**

<img width="995" height="196" alt="Screenshot 2025-11-11 at 17 04 37" src="https://github.com/user-attachments/assets/536adf9f-a004-43d9-9023-6b390ee18869" />


**This table shows which Windows Update settings under Advanced Options are changed and which are not**

| Setting | Configured Value | Rationale |
|----------|------------------|------------|
| Receive updates for other Microsoft products | ✅ On | It keeps Office, Defender, and other Microsoft software updated along with Windows. |
| Get me up to date | ❌ Off | It prevents forced reboots during critical tasks. Manually reboot after the updates |
| Download updates over metered connections | ❌ Off | Prevents bandwidth overuse. Avoid performing updates on non-metered networks, such as mobile hotspots, tethered data, or pay-per-GB internet |
| Notify me when a restart is required | ✅ On | Receive a notification to restart to complete the patch. |
| Active hours | 09:00–22:00 | Avoids interruptions during working hours. |
