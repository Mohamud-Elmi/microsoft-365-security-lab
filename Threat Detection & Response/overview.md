# 🧠 Threat Detection & Response

This section demonstrates how **Microsoft Defender for Business** and **Microsoft Defender for Endpoint** detect, investigate, and respond to threats in real time.  
The focus of this lab was validating that the integrated Microsoft 365 security stack could identify and remediate malware while feeding data into the organization’s threat analytics and secure score metrics.

---

## 🧩 Overview

After configuring endpoint protection and compliance in previous phases, this stage tested **Defender’s detection and response capabilities** using the industry-standard **EICAR test file**.  
This harmless simulation verified that the security controls and automated workflows were functioning correctly — from initial detection to quarantine and visibility in the security portal.

---

## 📸 Detection & Response Walkthrough

### 1. Malware Simulation (EICAR Test)  
**Screenshot:** `Malware-Detected.png`  
A simulated EICAR malware file was created and executed on the managed Windows 11 device (`USER1`).  
Defender’s **real-time protection** immediately detected the file and blocked execution before it could run.

### 2. Threat Notification  
**Screenshot:** `Threat-Found-Defender.png`  
Windows Security displayed a real-time alert confirming that a threat had been found and quarantined.  
This confirmed that the antivirus engine and behavioral monitoring were functioning as expected.

### 3. Incident Visualization  
**Screenshot:** `Malware-Detected.png` / `Incident graph`  
In the Microsoft 365 Security Portal, Defender automatically generated an incident graph linking the malicious file (`eicar.com`) to the affected host (`user1`).  
This provides analysts with an attack chain visualization, helping understand scope and impact.

### 4. Evidence & Response  
**Screenshot:** `Quarantine-File.png`  
The quarantined file was logged in the **Evidence and Response** section.  
Status showed **“Completed – Quarantined before investigation,”** indicating the threat was isolated automatically without requiring analyst action.

---

## 📊 Post-Incident Insights

### 5. Vulnerability Management Dashboard  
**Screenshot:** `Defender Vulnerability Dashboard.png`  
Defender Vulnerability Management evaluated the tenant’s security posture, scoring exposure risk at **58/100**.  
Recommendations included updating Windows, Edge, and ensuring real-time protection remained enabled — reflecting ongoing threat hygiene awareness.

### 6. Microsoft Secure Score  
**Screenshot:** `Secure Score.png`  
After the incident and policy enforcement, the organization’s Secure Score increased to **57.33%** overall, with notable improvements under *Device* and *Identity* categories.  
This metric provides a quantifiable measure of how Defender, Intune, and Entra configurations improve security maturity over time.

---

## 🧠 Key Takeaways

- **End-to-End Visibility:** Defender correlated endpoint data, threat detections, and device posture into a single incident view.  
- **Automated Containment:** Malware was blocked and quarantined instantly — proving that EDR and AV engines were fully operational.  
- **Continuous Improvement:** Secure Score and Vulnerability Management dashboards provide actionable insights to reduce attack surface.  
- **Enterprise-Grade Response Loop:** Alerts, quarantines, and post-incident analytics simulate real SOC workflows for small-to-medium business environments.

---

## ✅ Outcome

The Defender stack successfully detected, contained, and reported a simulated malware threat in real time.  
This confirms that the integrated Microsoft 365 security ecosystem — **Defender for Business**, **Intune**, and **Entra ID** — delivers a complete security lifecycle:  
**Prevention → Detection → Response → Continuous Hardening.**

---

*Next phase:* [🌐 Web & Phishing Defense](../Web%20&%20Phishing%20Defense/overview.md)

