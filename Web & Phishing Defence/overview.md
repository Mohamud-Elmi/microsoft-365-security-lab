# 🌐 Web & Phishing Defence

### Overview
This section demonstrates how **Microsoft Defender SmartScreen**, **Network Protection**, and **Enhanced Phishing Protection** combine to block unsafe websites, malicious downloads, and credential theft attempts. These features were configured through the **Windows Security Baseline** in Intune and automatically enforced by **Microsoft Defender for Business**.

### Configuration Summary
- **Network Protection:** Enabled in *Block Mode* to prevent access to malicious or low-reputation domains.  
- **SmartScreen for Microsoft Edge:** Enforced with prompts that cannot be bypassed.  
- **SmartScreen in Windows Shell:** Enabled to scan files and prevent unsafe executions.  
- **Enhanced Phishing Protection:** Actively warns users about password reuse, unsafe apps, and malicious activity.  
- **Web Content Filtering:** Enabled in Microsoft 365 Defender to block inappropriate or harmful sites organization-wide.

### Verification & Results
Testing on the Intune-managed Windows 11 VM confirmed that all controls were active and effective:

- Visiting Microsoft’s phishing demo site triggered the **SmartScreen red warning page** (`Reported Unsafe Site`).  
- Attempting to download a suspicious file (`freevideo.exe`) was **blocked as unsafe by Microsoft Edge**.  
- PowerShell verification showed `EnableNetworkProtection = 1`, confirming network protection was enforced.  
- The Microsoft 365 Defender portal displayed **Web Content Filtering** and **Network Protection** toggled on.

### Evidence
- `blocked page.png` — SmartScreen phishing site warning  
- `blocked download.png` — Unsafe file blocked in Edge  
- `smartscreen settings.png` — SmartScreen and phishing protection enabled  
- `edge smartscreen.png` — Edge browser SmartScreen configuration  
- `network protection.png` — Network Protection (Block Mode)  
- `web content filtering on.png` — Web Content Filtering enabled  

### Learning Outcome
This exercise demonstrated Microsoft’s multi-layered web defense approach, showing how SmartScreen, Network Protection, and phishing safeguards operate together. These settings ensure users are protected from web-based threats without relying on external gateways or browser extensions.

