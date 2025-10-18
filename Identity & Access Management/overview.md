# 🔐 Identity & Access Management

This section of the lab demonstrates how Microsoft Entra ID (formerly Azure AD) was configured to enforce secure identity management, multi-factor authentication, and role-based access control within the OvakraTest environment.

---

## 🧩 Overview

Identity and access management is the foundation of any Zero Trust architecture.  
In this lab, Entra ID was used to manage user identities, create dynamic security groups, enforce Conditional Access policies, and implement Multi-Factor Authentication (MFA) for all users — ensuring that access to Microsoft 365 services is both verified and controlled.

---

## 📸 Configuration Highlights

### 1. User and Role Setup  
**Screenshot:** `Users.png`, `Assigning Role.png`  
Created multiple user accounts (`IT Staff`, `User1`, `User2`, and `info@ElmiTestLab`) to simulate a small business environment.  
Assigned the **Security Administrator** role to the IT Staff account, enabling delegated management with the principle of least privilege.

### 2. Group Management  
**Screenshot:** `Entra Dynamic and Assigned Group.png`  
Configured three groups:
- **Admin Exclusion (No Conditional Access):** excludes key admin users from global CA policies during setup.  
- **All Company:** contains all standard users for policy targeting.  
- **Windows 11 Devices:** a **Dynamic Group** automatically populated based on OS criteria, enabling device-based policy automation.

### 3. Conditional Access Enforcement  
**Screenshot:** `Conditional Access Policy.png`  
Implemented three key Microsoft-managed Conditional Access policies:
- Block legacy authentication  
- Require MFA for admins  
- Require MFA for all users  

All policies are **enabled and enforced** to maintain secure sign-in posture and prevent high-risk authentication methods.

### 4. Multi-Factor Authentication (MFA) Configuration  
**Screenshot:** `MFA Enabled.png`  
Enabled Microsoft Authenticator for **all users**, allowing both passwordless and push-based verification.  
This ensures stronger identity protection across the tenant while maintaining user flexibility.

---

## 🧠 Key Takeaways

- **Zero Trust principle** applied — every access request is verified and conditional.  
- **Dynamic groups** reduce manual administration by automatically assigning devices or users based on rules.  
- **Role-based access control (RBAC)** enforces least-privilege permissions.  
- **MFA and Conditional Access** ensure users prove both identity and device compliance before accessing resources.

---

## ✅ Outcome

The Entra environment now supports secure, automated identity governance.  
Admins can manage users, roles, and policies centrally — achieving visibility and enforcement across all connected Microsoft 365 services.


