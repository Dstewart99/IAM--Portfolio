
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

🔗 [Microsoft Entra ID Labs](Entra-Labs)



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
**Goal:** Build hands-on, exam-level skills with Okta as an enterprise SSO, MFA, and lifecycle management platform, working toward the Okta Certified Professional certification. Labs are completed in a free Okta Developer Tenant and mapped directly to the Okta Certified Professional Performance Exam study guide.

🔗 [Okta Labs](Okta-Labs)

### 🔥 Topics Covered 

- User Management & Administration: Created user accounts manually in the Okta Admin Console, added custom profile attributes to the Universal Directory, edited user profiles, and managed account status. Created groups, manually assigned users, and built automated group rules to assign users based on profile attributes. Assigned a standard administrator role (Help Desk Admin) to a group and created a custom admin role with a scoped resource set to enforce least-privilege delegation.

- App Integration with SSO & Provisioning: Integrated an application from the Okta Integration Network (OIN) using SAML 2.0 Single Sign-On. Configured automated user provisioning (create, update, deactivate) from Okta to the downstream app. Assigned a group to the application and verified that users were automatically provisioned without manual intervention.


- Attribute Mapping & User Offboarding: Mapped Okta Universal Directory attributes to app-specific attributes using the Profile Editor and the Provisioning page. Practiced the offboarding workflow by deactivating a user account and verifying that access to all connected applications was immediately revoked, supporting the Leaver stage of the JML lifecycle.


- Security Policies & MFA Enforcement: Configured an authenticator (Okta Verify) and built an authenticator enrollment policy to require MFA for all users. Added rules to the Global Session Policy to enforce MFA at sign-in. Created an application-level Authentication Policy requiring step-up authentication for a high-value app. Set up a password policy with self-service account recovery options and verified that test users were prompted for the correct authenticators end-to-end.

 - Troubleshooting & System Log Analysis: Diagnosed and resolved common sign-in failures including locked accounts, deactivated users, and MFA enrollment issues. Expired user passwords and cleared active sessions from the Admin Console. Troubleshot app visibility issues caused by missing group assignments and incorrect group rules. Used the System Log (Reports > System Log) to search for and interpret authentication events, and identified the correct Okta support channels including the Support Portal, Okta Community, and Okta Status Page.




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


