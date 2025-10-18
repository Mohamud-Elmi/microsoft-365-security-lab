# 🧩 Microsoft 365 Security Lab

### 👨🏽‍💻 Author
**Mohamud Elmi**  
BSc Cybersecurity & Digital Forensics  
Building practical cybersecurity labs that bridge academic theory with enterprise-grade technical execution.  
[LinkedIn](https://www.linkedin.com/in/mohamud-elmi/) • [GitHub](https://github.com/Mohamud-Elmi/)

### Overview
This repository showcases a complete **Microsoft 365 Security Implementation Lab**, built to simulate how a small organization can deploy enterprise-grade protection using **Microsoft Intune**, **Defender for Business**, and **Entra ID**.  

The project demonstrates how identity, device, and endpoint security integrate under the **Zero Trust architecture**, guided by Microsoft’s security principles and the NIST Cybersecurity Framework (Identify → Protect → Detect → Respond → Recover).  

All configurations were deployed and verified in a **Microsoft 365 Business Premium** environment with managed **Windows 11 virtual machines**.

---

## 🔑 Lab Focus Areas

### 🔐 Identity & Access Management
Configuration of **Microsoft Entra ID (Azure AD)** to enforce strong identity controls and contextual access.  
**Key concepts applied:**
- **Zero Trust** → never trust, always verify  
- **Least privilege access** → Role-Based Access Control (RBAC)  
- **Defense in depth** → layered authentication policies  
- **Conditional Access** → enforcing sign-in rules based on risk and device compliance  

**Implemented controls:**
- Multi-Factor Authentication (MFA)  
- Device-based Conditional Access  
- Dynamic groups for automated onboarding  
- Role delegation with built-in Entra roles  

**References:**
- [Microsoft Learn – Identity & Access Management fundamentals](https://learn.microsoft.com/en-us/training/modules/describe-identity-concepts/)  
- [Zero Trust identity pillar – Microsoft Security](https://learn.microsoft.com/en-us/security/zero-trust/identity)  

**Goal:** Establish a secure identity perimeter that adapts to user risk and device health.  

---

### 💻 Device Management
Centralized management of Windows 11 endpoints using **Microsoft Intune** and the **Windows Security Baseline** to enforce compliance and configuration policies.  

**Key concepts applied:**
- **Hardening** through baselines and compliance policies  
- **Configuration drift prevention**  
- **Continuous assessment** using compliance states and reporting  
- **Security posture visibility** through Intune and Secure Score  

**Implemented controls:**
- Security Baseline deployment (Windows 10/11)  
- Compliance policies with conditional access enforcement  
- Device encryption, BitLocker, and Firewall monitoring  
- Automated remediation of non-compliant endpoints  

**References:**
- [Microsoft Endpoint Manager documentation](https://learn.microsoft.com/en-us/mem/intune/fundamentals/what-is-intune)  
- [CIS Microsoft 365 Benchmark Guidelines](https://www.cisecurity.org/benchmark/microsoft_365)  

**Goal:** Ensure only compliant and hardened devices connect to corporate resources.

---

### 🛡️ Endpoint Protection
Integration of **Microsoft Defender for Business** and **Defender for Endpoint** to secure endpoints with AI-driven protection, tamper prevention, and centralized management.  

**Key concepts applied:**
- **Defense-in-depth** endpoint architecture  
- **Attack Surface Reduction (ASR)**  
- **Firewall and threat protection baselines**  
- **Tamper Protection and automated remediation**  

**Implemented controls:**
- Real-time protection, behavior monitoring, and cloud protection  
- Defender Firewall configuration with logging  
- Tamper Protection enabled across endpoints  
- Endpoint onboarding through Intune and Defender portal  

**References:**
- [Microsoft Defender for Endpoint documentation](https://learn.microsoft.com/en-us/microsoft-365/security/defender-endpoint/)  
- [Attack Surface Reduction (ASR) overview](https://learn.microsoft.com/en-us/microsoft-365/security/defender-endpoint/attack-surface-reduction-rules-reference)  

**Goal:** Provide unified endpoint protection and visibility into threats through Defender’s central console.

---

### 🧠 Threat Detection & Response
Validation of **Defender for Endpoint’s** threat detection, alerting, and investigation capabilities through simulated malware incidents.  

**Key concepts applied:**
- **Threat intelligence correlation**  
- **Incident response lifecycle** (Detection → Analysis → Containment → Eradication → Recovery)  
- **SIEM/SOAR integration fundamentals**  
- **Forensic evidence tracking**  

**Implemented controls:**
- EICAR malware simulation to trigger incident alerts  
- Endpoint investigation and automated quarantine  
- Analysis of threat timeline, assets, and incident graphs  
- Review of evidence logs in the Defender portal  

**References:**
- [NIST SP 800-61 – Computer Security Incident Handling Guide](https://nvlpubs.nist.gov/nistpubs/SpecialPublications/NIST.SP.800-61r2.pdf)  
- [Microsoft Defender for Endpoint Investigation process](https://learn.microsoft.com/en-us/microsoft-365/security/defender-endpoint/investigate-alerts)  

**Goal:** Demonstrate proactive detection and response capabilities within the Microsoft 365 security ecosystem.

---

### 🌐 Web & Phishing Defense
Implementation of **Microsoft Defender SmartScreen**, **Network Protection**, and **Enhanced Phishing Protection** through Intune and Defender for Business.  

**Key concepts applied:**
- **Phishing defense and credential theft mitigation**  
- **DNS and URL-based content filtering**  
- **Browser isolation and risk categorization**  
- **User-centric defense mechanisms**  

**Implemented controls:**
- SmartScreen and Network Protection (block mode)  
- Enhanced phishing protection and password reuse detection  
- Web content filtering in Microsoft 365 Defender  
- Verification via phishing demo site and blocked download tests  

**References:**
- [Microsoft Defender SmartScreen overview](https://learn.microsoft.com/en-us/microsoft-edge/deploy/smartscreen)  
- [Web Threat Protection in Defender for Endpoint](https://learn.microsoft.com/en-us/microsoft-365/security/defender-endpoint/web-protection-overview)  

**Goal:** Prevent credential phishing, drive-by downloads, and malicious domain access.

---

## 🧾 Future Expansion
📈 **Documentation & Reporting:**  
Planned addition of Secure Score analysis, Intune compliance reports, and Defender exposure dashboards to visualize the organization’s evolving security posture.

---

### 🧰 Tools & Environment
- Microsoft 365 Business Premium tenant  
- Intune (Endpoint Manager)  
- Microsoft Defender for Business / Endpoint  
- Microsoft Entra ID (Azure AD)  
- Windows 11 Pro Virtual Machine (VirtualBox)  

---

### 🧩 Repository Structure
📂 microsoft-365-security-lab
┣ 📂 Identity & Access Management
┣ 📂 Device Management
┣ 📂 Endpoint Protection
┣ 📂 Threat Detection & Response
┣ 📂 Web & Phishing Defense
┣ 📜 LabBlueprint.md
┗ 📜 README.md

---

### 💬 Summary
This lab demonstrates a complete Microsoft 365 security ecosystem aligned with **Zero Trust principles**.  
It showcases the full journey — from identity governance to endpoint hardening and threat response — validating my understanding of modern **blue team**, **cloud administration**, and **cyber defense operations**.

