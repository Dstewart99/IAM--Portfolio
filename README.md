# Deandra Stewart | IAM Analyst Portfolio

**IT Help Desk → IAM Analyst** | 3+ yrs M365/Active Directory/Entra ID  
LinkedIn: https://www.linkedin.com/in/deandra-stewart-2301a6352

---
### About This Portfolio

This repository showcases my hands-on Identity & Access Management (IAM) labs in Microsoft Entra ID, focusing on cloud identity, access control, Conditional Access, Privileged Identity Management (PIM), SSPR, password protection, and MFA. It builds on my real-world experience managing identities in on-premises Active Directory.

### Active Directory Foundations (Professional Experience)

- Managed on-premises Active Directory user accounts and password resets in a fast-paced help desk environment.
- Created and updated security and distribution groups to control access to shared folders, mail, and line-of-business applications.
- Disabled accounts and removed group memberships for leavers as part of the Joiner–Mover–Leaver (JML) process, aligning with least-privilege principles.
- Performed new-hire onboarding by creating accounts, assigning group memberships, and ensuring access to required applications and shared resources as part of the Joiner process.
----
## 🎯 Goal

Document my hands-on identity labs and 30-day IAM study plan focused on:

- Joiner–Mover–Leaver (JML) lifecycle
- Least privilege, RBAC, and access reviews
- Microsoft Entra ID (Azure AD) and Active Directory
- Okta fundamentals (SSO/MFA) through self‑study labs

---

## 📂 Weekly Progress (WEEK 1)
**Goal:** Build a strong foundation in core IAM concepts and language.

- [Week 1 – IAM Foundations & MFA](week1/README.md)


### 🔥 Topics Covered
- IAM fundamentals: Identity, Authentication, Authorization, Governance, JML lifecycle.
- Access models: Principle of Least Privilege, Role-Based Access Control (RBAC), groups vs roles.
- Risk concepts: Segregation of Duties (SoD), excessive access, over‑provisioning, and real‑world risky access scenarios.
- Access reviews: Purpose of access certifications, why auditors require periodic reviews, and a basic access review workflow (who reviews what and how often).
- Identity Governance (IGA): How IGA extends IAM with approvals, policies, reviews, attestation, and SoD checks, plus a concise summary of “What is Identity Governance?”
  

## 📂 Weekly Progress (WEEK 2)
**Goal:** Build practical, hands‑on skills with Microsoft Entra ID while connecting it to my existing Active Directory experience, focusing on user and group management, access policies, admin roles, and identity protection features (SSPR, password protection, and MFA). 



Week 2–[Microsoft Entra ID labs](week2/README.md)

🔥 Topics Covered

- **Entra ID core objects and groups:** Created internal users and security groups (for example, IAM-Test-Employees), set properties like user type and usage location, and prepared groups for Conditional Access and PIM labs.  
- **Conditional Access basics:** Built a targeted policy that requires MFA for IAM-Test-Employees when accessing Microsoft Service Trust, and documented the policy behavior in plain language.  
- **Privileged Identity Management (PIM):** Compared just‑in‑time vs standing admin access, practiced eligible vs active role assignments, and activated/deactivated an eligible Security Reader role via PIM.  
- **Role-assignable groups and admin roles:** Created a role‑assignable group (IAM-User-Admins), assigned the User Administrator role to the group, and verified that membership controls who has that admin access.  
- **Self-Service Password Reset (SSPR):** Enabled SSPR for a lab group, configured authentication methods, registration (including 90‑day re‑confirmation), and reset notifications, then walked through the SSPR flow with a test user.  
- **Password Protection:** Configured smart lockout (threshold and duration), enabled a custom banned password list with organization-specific terms (Contoso, London, Widget), and enforced it to block weak passwords.  
- **Multifactor Authentication (MFA):** Enabled per‑user MFA for a lab user, reviewed MFA service settings, and configured MFA account lockout thresholds and timers to protect against MFA abuse.




## 📂 Weekly Progress (WEEK 3)
**Goal:** Get comfortable with Okta as an SSO and MFA platform.

### 🔥 Topics Covered
- Okta users and groups: Navigated the Okta Admin Console, created users and groups, and compared the user/group experience with Entra ID.
- App integrations and SSO basics: Reviewed what SSO is (SAML/OIDC at a high level), added a sample application to Okta, and documented the SSO flow in 4–5 steps.
- MFA policies: Explored Okta MFA factors, created or edited an MFA policy (who, when, which factor), and compared Okta MFA with Entra Conditional Access in a small table.
- Group rules and automation: Configured an Okta group rule to auto‑assign groups based on user attributes and tied this to JML automation.
- Okta vs Entra ID: Summarized key differences in integration style, strengths/use cases, and which system is treated as the “source of truth,” captured in a two‑column comparison.


## 📂 Weekly Progress (WEEK 4)
**Goal:** Connect IAM tools and concepts to real‑world IAM analyst responsibilities.

### 🔥 Topics Covered
- IAM analyst daily work: Described typical tasks such as handling JML tickets, managing access requests and approvals, and performing access reviews and cleanup in a “day in the life” outline.
- Access request workflows: Broke down the request → approval → provisioning → verification flow and identified key roles involved (requestor, manager, approver, IAM team).
- Birthright vs privileged access: Defined birthright access with examples (email, baseline apps) and privileged access with examples (admin portals, security tools), then mapped current help desk permissions to each.
- Insider risk and access abuse: Reviewed types of insider threats (malicious, accidental, compromised accounts) and wrote scenarios showing how IAM controls reduce risk.
- Compliance basics: Covered high‑level concepts for SOX, HIPAA, and audits, and explained how IAM supports compliance through JML, least privilege, and periodic access reviews.


## 📂 Weekly Progress (WEEK 5)
**Goal:** Turn skills into interviews with strong stories, a focused resume, and practiced scenarios.

### 🔥 Topics Covered
- IAM storytelling: Wrote and practiced a 60–90 second explanation of “What is IAM?” and “What does an IAM analyst do?” out loud.
- Scenario practice: Prepared structured answers (Situation → Risk → Action → Outcome) for common IAM scenarios like inappropriate access requests, urgent admin rights, and discovering excessive access.
- IAM resume bullets: Translated current help desk work into IAM language (JML, MFA support, group/access management) and added quantified bullets highlighting Entra and Okta labs.
- Full review: Revisited IAM fundamentals, Entra ID labs, and Okta labs, tightening and clarifying notes where needed.
- Mock interview: Practiced core interview questions (“Tell me about yourself” with an IAM angle, JML, least privilege, Okta vs Entra ID) and recorded a mock interview for self‑review.


---

## 🧠 Core IAM Skills

- **Identity lifecycle:** Joiner–Mover–Leaver (provisioning, access changes, deprovisioning).
- **Access control:** Least privilege, RBAC, Segregation of Duties (SoD).
- **Microsoft stack:** Active Directory and Entra ID (users, groups, Conditional Access, basic PIM).
- **In progress:** Okta fundamentals (SSO, MFA, group rules) through labs and self‑study.
- **Operations:** 3+ years handling daily access requests and identity tickets in an M365/AD-heavy help desk environment.


