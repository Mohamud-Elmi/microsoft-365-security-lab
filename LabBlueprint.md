# 🧾 Microsoft 365 Security Lab – Project Overview

This project documents the design and deployment of a hands-on **Microsoft 365 Security Lab**, built to simulate a real-world enterprise environment.
The goal is to demonstrate practical understanding of **Microsoft Entra ID**, **Intune**, and **Defender for Business** — from identity management to endpoint protection and threat detection.

The lab was configured within a Microsoft 365 Business Premium tenant using a Windows 11 virtual machine enrolled in Intune.
All configurations were applied in a controlled test environment to explore Microsoft’s modern security ecosystem safely.

The project is divided into **seven structured phases**, each focusing on a core area of the Microsoft 365 security stack:

1. Entra ID — Identity & Access Management
2. Intune — Device Management & Compliance
3. Defender for Business — Endpoint Protection
4. EDR & Vulnerability Management — Threat Detection & Response
5. Compliance & Conditional Access — Risk-Based Enforcement
6. Web & Phishing Protections — User and Web Security
7. Documentation & Reporting — Operational Output and Review

Each phase includes objectives, implementation steps, verification methods, and outcomes, supported by screenshots and documentation stored in the `/Evidence` and `/Documents` folders.

Perfect — here’s your **7-phase sequence** (the official order you’ll document in `LabBlueprint.md`).
This version is written cleanly for your GitHub — concise, professional, and formatted for Markdown.

# 🧩 Microsoft 365 Security Lab — 7 Phases

This lab project demonstrates a full Microsoft 365 Business Premium security environment built from scratch, covering identity, device management, and endpoint protection.

---

## **Phase 1 — Entra ID (Identity Foundation)**

**Objective:**
Establish a secure and organized identity layer for users, admins, and devices.

**Core Tasks:**

* Create Admin and Test User accounts (`admin@`, `user1@`, `user2@`).
* Apply least-privilege roles (Security Admin / Reader only).
* Enable Multi-Factor Authentication (MFA).
* Build **dynamic device/user groups** for targeting Intune policies.
* Understand **device states** (Entra Joined, Registered, Hybrid).

**Outcome:**
A hardened identity base with MFA, controlled admin access, and logical device grouping.

---

## **Phase 2 — Intune (Device Management Backbone)**

**Objective:**
Establish central device management and enforce basic compliance.

**Core Tasks:**

* Enroll the Windows 11 VM into Intune.
* Import the **Microsoft Security Baseline** or **Open Intune Baseline**.
* Configure **Compliance Policies** (BitLocker, OS version, no local admin).
* Test assignment of profiles to dynamic groups.

**Outcome:**
Devices are managed and compliant through Intune — forming the policy delivery layer for all future configurations.

---

## **Phase 3 — Defender for Business (Protection Layer)**

**Objective:**
Deploy core protection across managed devices using Defender for Business.

**Core Tasks:**

* Connect **Defender ↔ Intune** for automatic onboarding.
* Deploy:

  * **Next-Gen Antivirus**
  * **Firewall**
  * **Attack Surface Reduction (ASR)** (audit mode first)
  * **Tamper Protection**
* Configure **email alert rules** in the Defender portal.

**Outcome:**
Endpoints are onboarded, protected, and reporting telemetry into the Microsoft 365 Defender portal.

---

## **Phase 4 — Detection & Vulnerability Management (EDR + Auto-Remediation)**

**Objective:**
Enable advanced endpoint detection, auto-remediation, and vulnerability intelligence.

**Core Tasks:**

* Confirm **EDR + Auto-IR** are active (default in Defender for Business).
* Simulate detection (EICAR test file).
* Explore **Vulnerability Management** dashboards.
* Test **automatic remediation** and track exposure score.

**Outcome:**
Live endpoint detection and automated response capabilities verified through incident testing.

---

## **Phase 5 — Compliance + Conditional Access (Risk-Based Enforcement)**

**Objective:**
Integrate Defender risk scoring with Conditional Access to enforce Zero Trust principles.

**Core Tasks:**

* Configure **Device Compliance Policy** (require device risk ≤ Medium).
* Create **Conditional Access Policy**:

  * Require compliant device & MFA.
  * Exclude break-glass admin.
* Test policy using VM and host machine for comparison.

**Outcome:**
Only compliant, secure devices can access Microsoft 365 resources — unsafe devices are automatically blocked.

---

## **Phase 6 — Web & Phishing Protections**

**Objective:**
Harden endpoint web access and user behavior against phishing and malicious sites.

**Core Tasks:**

* Enable **SmartScreen** and **PUA Blocking** via Intune Settings Catalog.
* Enable **Enhanced Phishing Protection** (Windows 11 22H2+).
* Configure **Web Content Filtering** in Defender portal (block risky categories).

**Outcome:**
Safer browsing, password protection, and reduced exposure to malicious or deceptive websites.

---

## **Phase 7 — Documentation & Reporting**

**Objective:**
Consolidate all configurations, screenshots, and outcomes into professional documentation.

**Core Tasks:**

* Document each completed phase with screenshots under `/Evidence/`.
* Create a **Monthly Security Report Template** (showing incidents, compliance, and recommendations).
* Write **Lessons Learned / SOPs** in `/Documents/`.
* Export **Secure Score** and summary graphs for visual proof.

**Outcome:**
A complete technical record demonstrating Microsoft 365 security deployment and operational documentation skills.

---

## ✅ Summary Flow

**Entra ID → Intune → Defender → EDR → Compliance/CA → Web Protections → Documentation**

Or conceptually:

> **Identity → Management → Protection → Detection → Enforcement → Hardening → Reporting**

Here’s the perfect **closing paragraph** for the end of your `LabBlueprint.md` — professional, reflective, and written to impress hiring managers or technical interviewers who might view your GitHub.

It closes the project naturally and shows that you understand the real-world purpose behind the lab.

---

## 🧩 Project Reflection & Conclusion

This lab represents a complete, end-to-end deployment of Microsoft’s modern security stack — from **identity** to **incident response**.
By building each layer manually, I gained a deeper understanding of how Microsoft 365 components interconnect to form a Zero Trust environment:

* **Entra ID** secures identity and access.
* **Intune** governs devices and enforces compliance.
* **Defender for Business** provides continuous protection, detection, and response.

Throughout the project, I focused on **real-world configurations**, **controlled testing**, and **documented outcomes** — the same processes used by security professionals managing live tenants.
This approach helped solidify practical skills in deploying and maintaining enterprise-grade security across the Microsoft ecosystem.

The documentation within this repository is designed to show transparency, structure, and repeatability — essential qualities for working in blue team, SOC, or managed security operations roles.
As I continue to refine and expand this lab, it will evolve into a comprehensive personal reference for Microsoft 365 security architecture and operational defense.
