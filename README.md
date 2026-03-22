
### About This Portfolio

This repository showcases my hands-on Identity & Access Management (IAM) labs in Microsoft Entra ID and Okta, focusing on cloud identity, access control, Conditional Access and Okta policies, Privileged Identity Management (PIM), self-service password reset (SSPR), password protection, and multi-factor authentication (MFA). It builds on my real-world experience managing identities in on-premises Active Directory and extending those skills into modern cloud identity platforms.

### Active Directory Foundations (Professional Experience)

- Managed on-premises Active Directory user accounts and password resets in a fast-paced help desk environment.
- Created and updated security and distribution groups to control access to shared folders, mail, and line-of-business applications.
- Disabled accounts and removed group memberships for leavers as part of the Joiner–Mover–Leaver (JML) process, aligning with least-privilege principles.
- Performed new-hire onboarding by creating accounts, assigning group memberships, and ensuring access to required applications and shared resources as part of the Joiner process.
----

## 🎯 Goal

Document my hands-on identity labs IAM study plan focused on:

- Joiner–Mover–Leaver (JML) lifecycle
- Least privilege, RBAC, and access reviews
- Microsoft Entra ID (Azure AD) and Active Directory
- Okta fundamentals (SSO/MFA) through self‑study labs

---
## IAM Foundations

Before diving into Entra ID and Okta labs, I documented my core IAM and Identity Governance concepts (identity, authentication, authorization, JML, least privilege, access reviews, and IGA) here:

👉 [View IAM Foundations](IAM-foundations)


 ---

  
## 📂 Identity Labs: Microsoft Entra ID
**Goal:** Build practical, hands‑on skills with Microsoft Entra ID while connecting it to my existing Active Directory experience, focusing on user and group management, access policies, admin roles, and identity protection features (SSPR, password protection, and MFA). 

🔗 [Microsoft Entra ID Labs](entra-id-labs)


🔥 Topics Covered

- **Entra ID core objects and groups:** Created internal users and security groups (for example, IAM-Test-Employees), set properties like user type and usage location, and prepared groups for Conditional Access and PIM labs.  
- **Conditional Access basics:** Built a targeted policy that requires MFA for IAM-Test-Employees when accessing Microsoft Service Trust, and documented the policy behavior in plain language.  
- **Privileged Identity Management (PIM):** Compared just‑in‑time vs standing admin access, practiced eligible vs active role assignments, and activated/deactivated an eligible Security Reader role via PIM.  
- **Role-assignable groups and admin roles:** Created a role‑assignable group (IAM-User-Admins), assigned the User Administrator role to the group, and verified that membership controls who has that admin access.  
- **Self-Service Password Reset (SSPR):** Enabled SSPR for a lab group, configured authentication methods, registration (including 90‑day re‑confirmation), and reset notifications, then walked through the SSPR flow with a test user.  
- **Password Protection:** Configured smart lockout (threshold and duration), enabled a custom banned password list with organization-specific terms (Contoso, London, Widget), and enforced it to block weak passwords.  
- **Multifactor Authentication (MFA):** Enabled per‑user MFA for a lab user, reviewed MFA service settings, and configured MFA account lockout thresholds and timers to protect against MFA abuse.


-----------------

## 📂 Identity Labs: Okta
**Goal:** Get comfortable with Okta as an SSO and MFA platform.

[OKTA](week2)
### 🔥 Topics Covered 

- **Admin Console & Foundations:** Explored the Okta Admin Console layout (Dashboard, Directory, Applications, Security, Workflow, Reports) and mapped key features to the four exam domains.

- **Universal Directory & Profiles:** Practiced creating user profiles with standard and custom attributes, configuring profile mappings between Okta and app profiles, and understanding attribute types and profile mastering. 

- **AD Integration & Lifecycle:** Reviewed Okta AD Agent architecture, import and matching rules, delegated authentication behavior, and JIT vs. scheduled imports, then walked through troubleshooting scenarios. 

- **Groups, Rules, and Group Push:** Created Okta, AD-sourced, and app groups, built group rules to auto-assign users based on attributes, and tested group push to downstream applications.  

- **SSO & Federation Protocols:** Configured a SAML application in the dev tenant, tested SP-initiated and IdP-initiated flows, and reviewed SAML, OIDC, SWA, and OIN integration concepts. 

- **Provisioning & Automation:** Enabled provisioning for an app (create, update, deactivate), validated auto-deprovisioning behavior, and implemented lifecycle automation with group-based assignments. 

- **Security, MFA, and Policies:** Created MFA enrollment and sign-on policies, compared factor types, and practiced policy hierarchy and precedence for secure access control. 

- **Admin Roles, Self-Service, and Operations:** Reviewed admin roles (Super Admin, Org Admin, App Admin, Help Desk Admin), end-user self-service features, mobile options (Okta Mobile vs OMM), API tokens, System Log, and reporting. 



## 📂 IAM in Practice
**Goal:** Connect IAM tools and concepts to real‑world IAM analyst responsibilities.

### 🔥 Topics Covered
- IAM analyst daily work: Described typical tasks such as handling JML tickets, managing access requests and approvals, and performing access reviews and cleanup in a “day in the life” outline.
- Access request workflows: Broke down the request → approval → provisioning → verification flow and identified key roles involved (requestor, manager, approver, IAM team).
- Birthright vs privileged access: Defined birthright access with examples (email, baseline apps) and privileged access with examples (admin portals, security tools), then mapped current help desk permissions to each.
- Insider risk and access abuse: Reviewed types of insider threats (malicious, accidental, compromised accounts) and wrote scenarios showing how IAM controls reduce risk.
- Compliance basics: Covered high‑level concepts for SOX, HIPAA, and audits, and explained how IAM supports compliance through JML, least privilege, and periodic access reviews.





---

## 🧠 Core IAM Skills

- **Identity lifecycle:** Joiner–Mover–Leaver (provisioning, access changes, deprovisioning).
- **Access control:** Least privilege, RBAC, Segregation of Duties (SoD).
- **Microsoft stack:** Active Directory and Entra ID (users, groups, Conditional Access, basic PIM).
- **In progress:** Okta fundamentals (SSO, MFA, group rules) through labs and self‑study.
- **Operations:** 3+ years handling daily access requests and identity tickets in an M365/AD-heavy help desk environment.


