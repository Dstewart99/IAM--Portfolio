## IAM Foundations for Analysts

### 🎯 Objective  
Build a strong understanding of core Identity and Access Management (IAM) and Identity Governance concepts, and connect them to real-world identity lifecycle operations in enterprise environments.

---

### 🔐 Core Identity Concepts  

| Concept        | Definition                                           | Why It Matters in Organizations                                      |
|----------------|------------------------------------------------------|-----------------------------------------------------------------------|
| Identity       | A digital representation of a user or account.       | All access decisions depend on accurate, unique identities.  |
| Authentication | Verifying who a user is (password, MFA, biometrics). | Prevents unauthorized access through credential abuse.       |
| Authorization  | Determining what a user is allowed to access.        | Enforces least privilege and limits security risk.          |
| Governance     | Oversight of access through policies, approvals, and reviews. | Required for audits, compliance, and risk reduction.|

---

### 🔄 Joiner–Mover–Leaver (JML) Lifecycle  

Identity access changes throughout a user’s employment lifecycle.

| Stage  | IAM Activities                                         | Risk if Not Managed                                        |
|--------|--------------------------------------------------------|------------------------------------------------------------|
| Joiner | Account creation, license assignment, MFA enrollment.  | Over-provisioning and unnecessary access at onboarding.[web:26] |
| Mover  | Updating group memberships and roles.                  | Permission/privilege creep from old access not removed.[web:28][web:31] |
| Leaver | Disabling accounts and revoking access.                | Orphaned accounts and potential security breaches.[web:25][web:31] |

**Connection to my role:**  
I regularly support JML processes through user provisioning, license assignment, MFA troubleshooting, and group membership updates in enterprise environments.

---

### 🛡 Least Privilege & RBAC  

- **Least Privilege** ensures users only receive the access required for their job, reducing the impact of compromised accounts or mistakes.
- **Role-Based Access Control (RBAC)** assigns permissions through roles or groups instead of directly to individuals, simplifying management at scale.

**Enterprise application example:**

- New hires receive access through department-based security groups.  
- Role changes trigger group membership and role updates.  
- Offboarding removes group memberships and disables accounts so access is revoked across systems.

This approach improves scalability, reduces errors, and strengthens the organization’s security posture.

---

### ⚠ Risk Concepts in IAM  

**Segregation of Duties (SoD)**  
SoD prevents one user from controlling an entire high-risk process by separating conflicting responsibilities (for example, requesting and approving the same transaction).
Example: End users can operate applications, but only IT admins can install or approve software. This separation reduces fraud, misuse, and accidental changes.

**Excessive Access & Permission Creep**  
Access accumulates over time when permissions are not removed after role or project changes, leading to excessive access and “privilege creep.” 

Common risk scenarios:

- End user with unnecessary local admin rights on their workstation.  
- Former team member retaining access to shared mailboxes or SharePoint sites.  
- Contractor accounts maintaining elevated privileges after the contract ends.

---

### 🔍 Access Reviews  

Access certifications (access reviews) validate that users still require their assigned access and help organizations remediate unnecessary permissions.

| Element | Description                                             |
|---------|---------------------------------------------------------|
| Who     | Managers and application or resource owners.            |
| What    | Verify group memberships, role assignments, and app access. |
| When    | Quarterly for high-risk systems, at least annually for others. |

Access reviews help organizations control permission creep and demonstrate effective access control for compliance and audits.

---

### 🧩 Identity Governance (IGA)  

| IAM                                                   | IGA                                                             |
|-------------------------------------------------------|-----------------------------------------------------------------|
| Manages identities and access (authentication, authorization, access control). | Governs how access is approved, reviewed, and monitored over time.
| Focuses on enforcing access policies (e.g., RBAC, MFA).        | Focuses on policies, approvals, reviews, SoD, and reporting.

IGA commonly adds:

- Access request and approval workflows.  
- Periodic access reviews across key applications and groups.  
- SoD analysis to catch risky combinations of roles and entitlements.  
- Compliance reporting to show that access is appropriate and reviewed.

Identity Governance ensures access stays aligned with job roles and regulatory requirements as users join, move, and leave the organization.

---

### 🧠 Key Takeaway  

Strong IAM practice combines:

- Technical controls (authentication, RBAC, MFA).  
- Lifecycle management (Joiner–Mover–Leaver).  
- Governance processes (access reviews, approvals, SoD controls).

This foundation supports secure and compliant identity management across enterprise environments and sets the stage for the Azure Entra ID and Okta labs that follow.

