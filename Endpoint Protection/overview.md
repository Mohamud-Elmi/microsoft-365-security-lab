# 🛡️ Endpoint Protection

This section focuses on endpoint security configuration and protection through **Microsoft Defender for Business** integrated with **Intune** and **Microsoft Defender for Endpoint**.  
The goal of this lab phase was to establish a unified threat prevention, detection, and response framework for managed devices.

---

## 🧩 Overview

Endpoint protection ensures that every enrolled device maintains strong, layered defense against malware, network intrusion, and configuration tampering.  
The lab environment simulates a modern security posture for small-to-medium enterprises using Microsoft 365 Business Premium.

Key objectives:
- Enforce Defender Antivirus, Firewall, and Cloud Protection
- Connect Intune-managed devices to Microsoft Defender for Endpoint
- Validate EDR visibility and Tamper Protection
- Demonstrate centralized policy enforcement through Intune

---

## 📸 Configuration Highlights

### 1. Defender Antivirus Configuration  
**Screenshot:** `realtime monitoring.png`  
Enabled real-time monitoring, cloud protection, and behavioral analysis via the **Windows Security Baseline**.  
This ensures continuous scanning of all files, removable drives, and scripts, providing proactive defense against malware.

### 2. Defender Firewall Enforcement  
**Screenshot:** `firewall.png`  
Configured Defender Firewall settings to block inbound connections by default while logging successful and dropped packets.  
This configuration adds an essential perimeter control, especially for non-domain devices.

### 3. Tamper Protection  
**Screenshot:** `Tamper Protection.png`  
Enabled **Tamper Protection** to prevent unauthorized modifications to Defender and Intune security settings.  
Even local administrators are blocked from disabling real-time monitoring, behavior analysis, or cloud protection — a key safeguard against insider tampering or malware attempting to disable protection.

### 4. Defender for Endpoint Integration  
**Screenshots:** `Endpoint Security Connection.png`, `Defender-Intune-connected.png`  
The **Microsoft Defender for Endpoint** connector was successfully established with Intune.  
This allows security configurations and telemetry to flow seamlessly between both platforms, enabling unified visibility, automated investigations, and compliance-based access control.

---

## 🧠 Key Takeaways

- **Unified Endpoint Protection:** Defender AV, Firewall, and Cloud Protection policies are centrally managed via Intune.  
- **Strong Device Integrity:** Tamper Protection ensures that security settings cannot be overridden locally.  
- **Integrated EDR Visibility:** Defender for Endpoint provides incident correlation, asset inventory, and attack surface reduction telemetry.  
- **Automation-Ready Setup:** The Intune–Defender link enables automatic remediation and conditional compliance enforcement.

---

## ✅ Outcome

Through these configurations, endpoints in the lab achieved **enterprise-grade protection** equivalent to what’s deployed in real SMB environments using Microsoft 365 Business Premium.  
All security baselines, policies, and telemetry now operate cohesively to detect, prevent, and respond to modern threats in real time.

---

*Next phase:* [🧠 Threat Detection & Response](../Threat%20Detection%20&%20Response/overview.md)

