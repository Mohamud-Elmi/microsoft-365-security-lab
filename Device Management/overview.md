# 💻 Device Management

This section focuses on Microsoft Intune configuration, compliance policies, and device baselines to enforce secure management of enrolled endpoints in the OvakraTest tenant.

---

## 🧩 Overview

Device management ensures that all endpoints accessing corporate data meet the organization’s security requirements.  
In this lab, Microsoft Intune was used to enroll Windows 11 test devices, apply security baselines, and verify compliance enforcement through Conditional Access integration.

---

## 📸 Configuration Highlights

### 1. Device Enrollment and Management  
**Screenshot:** `Intune Device Enrolled and Compliant.png`  
A Windows 11 virtual machine (`USER1`) was successfully onboarded into Intune.  
Device ownership was set to **Corporate**, and compliance reporting confirmed that the device was actively managed by Intune.

### 2. Security Baseline Application  
**Screenshot:** `Security Baseline Applied.png`  
Applied the **Windows Security Baseline – Lab (v24H2)** to standardize system configuration according to Microsoft’s recommended best practices.  
This included enforcing BitLocker, secure boot, and Defender Antivirus settings to align with enterprise security benchmarks.

### 3. Compliance Policy Enforcement  
**Screenshot:** `Compliance Policy.png`, `Not-Compliant.png`, `compliance report.png`  
Configured a **Windows 11 Compliance Policy** that monitors device posture and marks devices as **Non-Compliant** when critical protections (e.g., Real-time Protection) are disabled.  
This ensures that misconfigured or insecure devices are immediately restricted from accessing organizational resources.

### 4. Conditional Access Integration  
**Screenshot:** `M365 Access Denied.png`  
When the test device failed compliance due to disabled real-time protection, Conditional Access automatically blocked sign-in to Microsoft 365 resources.  
This validated the full end-to-end compliance enforcement pipeline — from device health monitoring in Intune to access control in Entra ID.

---

## 🧠 Key Takeaways

- **Unified Device Visibility:** All managed endpoints report to Intune with real-time compliance data.  
- **Automated Security Enforcement:** Devices must meet baseline configurations before gaining access.  
- **Integrated Compliance & Access Control:** Non-compliant devices are blocked from Microsoft 365 resources through Conditional Access.  
- **Demonstrated Endpoint Governance:** This workflow simulates real-world enterprise device compliance processes used by IT security teams.

---

## ✅ Outcome

Through this exercise, the Intune environment achieved a full compliance loop:
1. Device enrolled  
2. Security baseline applied  
3. Compliance evaluated  
4. Conditional Access enforced  

This demonstrates how Microsoft 365 Business Premium can effectively secure and manage modern workplace endpoints at scale.


