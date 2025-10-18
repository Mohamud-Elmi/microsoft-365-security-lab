# 🧭 Microsoft 365 Security Lab Blueprint

### Overview
This lab blueprint outlines the structure, configuration flow, and learning outcomes behind the **Microsoft 365 Security Lab**.  
It was designed to simulate a real-world small business environment using **Microsoft 365 Business Premium**, **Intune**, **Defender for Business**, and **Entra ID** — aligning with **Zero Trust** and **NIST Cybersecurity Framework** principles.  

---

## ⚙️ Environment Setup

**Platform:** Microsoft 365 Business Premium (trial tenant)  
**Virtual Environment:** Windows 11 Pro (VirtualBox)  
**Management Tools:** Microsoft Intune, Defender for Endpoint, Entra ID  

**Test Accounts:**
- `admin@elmitestlab.onmicrosoft.com` — Global Admin  
- `user1@elmitestlab.onmicrosoft.com` — Standard User (Enrolled Device)  
- `user2@elmitestlab.onmicrosoft.com` — Secondary User  

**Devices:**
- Windows 11 VM (Intune-enrolled and onboarded to Defender)  
- Managed via compliance policies and security baselines  

---

## 🧩 Phase 1: Identity & Access Management

**Objective:**  
Implement identity security controls through **Microsoft Entra ID** to protect user authentication and resource access.

**Configuration Steps:**
1. Enabled **Multi-Factor Authentication (MFA)** for user sign-ins.  
2. Created **Conditional Access** policies requiring compliant devices and MFA.  
3. Set up **Dynamic Groups** for automatic policy assignment based on device platform.  
4. Assigned roles using **Role-Based Access Control (RBAC)** principles.

**Concepts Applied:**  
- Zero Trust identity model  
- Least privilege access  
- Contextual authentication  
- Automated identity governance  

**Outcome:**  
Unauthorized or non-compliant devices are denied access; all logins require MFA.  

---

## 💻 Phase 2: Device Management

**Objective:**  
Use **Microsoft Intune** to enforce baseline configurations and compliance monitoring for enrolled devices.  

**Configuration Steps:**
1. Enrolled the Windows 11 VM into **Intune**.  
2. Applied the **Windows Security Baseline** to harden system configurations.  
3. Created **Compliance Policies** enforcing encryption, firewall, and antivirus status.  
4. Configured **Device Remediation** and compliance reporting in the Intune dashboard.

**Concepts Applied:**  
- Endpoint hardening and posture management  
- Configuration drift prevention  
- Policy-based access control  
- Continuous monitoring  

**Outcome:**  
Devices must meet baseline and compliance standards before gaining access to cloud resources.  

---

## 🛡️ Phase 3: Endpoint Protection

**Objective:**  
Integrate **Microsoft Defender for Business** and **Defender for Endpoint** for advanced endpoint protection and telemetry visibility.  

**Configuration Steps:**
1. Connected Defender for Endpoint with Intune (Endpoint Security Connector).  
2. Enabled **Tamper Protection** and **Behavior Monitoring**.  
3. Configured Defender Firewall and Logging.  
4. Validated EDR connectivity in the **Defender Security Center**.

**Concepts Applied:**  
- Defense in depth  
- Attack surface reduction  
- Real-time protection  
- Endpoint telemetry and threat prevention  

**Outcome:**  
Endpoints receive enterprise-grade protection with centralized management and visibility.  

---

## 🧠 Phase 4: Threat Detection & Response

**Objective:**  
Test and validate Defender for Endpoint’s detection and incident response capabilities using controlled malware simulations.

**Configuration Steps:**
1. Deployed the **EICAR test file** to trigger Defender alerts.  
2. Verified quarantine and alert generation in the **Defender portal**.  
3. Analyzed the incident graph, evidence timeline, and affected assets.  
4. Observed Secure Score and exposure score improvements post-mitigation.

**Concepts Applied:**  
- Threat detection and investigation  
- Incident response lifecycle (Detect → Analyze → Contain → Remediate)  
- Forensic evidence handling  
- Security posture analytics  

**Outcome:**  
Defender automatically detected and quarantined the malicious file, generating incident reports and asset correlation data.  

---

## 🌐 Phase 5: Web & Phishing Defense

**Objective:**  
Implement and test **SmartScreen**, **Enhanced Phishing Protection**, and **Network Protection** through Intune and Defender.  

**Configuration Steps:**
1. Enabled **Network Protection (block mode)** and **SmartScreen** via the security baseline.  
2. Turned on **Enhanced Phishing Protection** and password reuse detection.  
3. Activated **Web Content Filtering** in Microsoft 365 Defender.  
4. Tested via phishing demo site and unsafe download simulation.

**Concepts Applied:**  
- Web content filtering and URL reputation  
- Browser-level phishing mitigation  
- Credential theft prevention  
- Endpoint web protection telemetry  

**Outcome:**  
Malicious websites and downloads were blocked automatically by SmartScreen and Defender policies.  

---

## 📊 Phase 6: Documentation & Reporting (Planned)

**Objective:**  
Document and evaluate overall security posture through analytics and compliance reporting.

**Planned Steps:**
- Capture Secure Score improvements across Identity, Device, and App pillars.  
- Export Intune compliance reports and Defender exposure dashboards.  
- Create executive-style summaries for management or client demonstration.  

**Concepts to Apply:**  
- Compliance auditing  
- Posture management  
- Continuous improvement via Secure Score metrics  

---

## 🧱 Architecture Overview

**Integration Flow:**
[ User Identity (Entra ID) ]
↓ MFA / Conditional Access
[ Device Management (Intune) ]
↓ Security Baselines / Compliance
[ Endpoint Protection (Defender) ]
↓ Telemetry & Threat Response
[ Web Protection & Phishing Defense ]
↓
[ Centralized Reporting (Defender Portal + Secure Score) ]


This architecture reflects Microsoft’s **Zero Trust Framework**:  
> “Verify explicitly, use least privilege, and assume breach.”

---

## 📘 References
- [Microsoft Learn – Security, Compliance, and Identity Fundamentals](https://learn.microsoft.com/en-us/training/paths/sc-900-security-compliance-identity-fundamentals/)  
- [NIST Cybersecurity Framework (CSF)](https://www.nist.gov/cyberframework)  
- [Microsoft Zero Trust Model](https://learn.microsoft.com/en-us/security/zero-trust/)  
- [CIS Microsoft 365 Benchmark](https://www.cisecurity.org/benchmark/microsoft_365)  

---

### ✅ Learning Outcomes
By completing this lab, the following skills and concepts were demonstrated:
- Practical implementation of Zero Trust architecture  
- Identity governance and MFA enforcement  
- Endpoint hardening through Intune and Defender baselines  
- Threat detection and incident response analysis  
- Web and phishing protection testing  
- Secure Score posture improvement tracking  

---

**Author:**  
**Mohamud Elmi**  
_BSc Cybersecurity & Digital Forensics_  
