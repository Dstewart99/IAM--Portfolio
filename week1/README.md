### ✅ IAM Foundations

- Defined Identity, Authentication, Authorization, and Governance.
- Learned the Joiner–Mover–Leaver (JML) lifecycle and wrote examples from my help desk work.
- Created and reviewed IAM flashcards for these core terms:
  
  - Identity: Who the user/account is.
  - Authentication: Proving identity (password, MFA).
  - Authorization: What the user is allowed to access.
  - Governance: Policies, approvals, and reviews that control access.
  - JML: Joiner (new hire), Mover (role change), Leaver (offboarding).
 
### ✅ Day 2 – Least Privilege & RBAC

- Reviewed the principle of least privilege and role-based access control (RBAC), focusing on giving users only the minimum access needed to perform their job duties.
- Compared how security groups in Active Directory and roles in Microsoft Entra ID can both be used as building blocks for RBAC instead of granting permissions user-by-user.
  
- Documented 3 real access scenarios from my help desk experience and described how RBAC would handle them:
  
  - New hire: Assign the user to department and job function groups so they automatically get access to the correct apps and shared resources.
  - Role change (mover): Remove the user from old role/department groups and add them to new ones so their access updates with their job.
  - Offboarding (leaver): Disable the account and remove group memberships to ensure access is revoked across all linked systems.



### ✅ Day 3 – Risk Concepts

- Defined Segregation of Duties (SoD) as splitting high‑risk steps between different roles so one person cannot control an entire process.
- Example: regular end users can use applications on their laptops, but only IT admins are allowed to install or approve new software. This separates “using” from “controlling” the software.

- Reviewed excessive access and over‑provisioning risk, including how users can slowly collect permissions over time when they change roles but old access is never removed.
  
- Noted 3 example risky access scenarios:
      - An end user has local admin rights on their workstation and can install any software they want, increasing malware and data exfiltration risk.
       -A former project member still has access to a shared mailbox and SharePoint site with sensitive files months after leaving the team.
       - A contractor account keeps high‑privilege directory or admin permissions after their contract ends instead of being downgraded or disabled.
 

### ✅ Day 4 – Access Reviews

- Learned that access certifications (user access reviews) are periodic checks where managers or system owners verify that each user still needs their current access and revoke anything that is no longer required.
- Noted that auditors and regulations expect periodic access reviews (often quarterly or annually) to prove that the company is controlling permission creep and removing unnecessary or risky access over time.
  
- Wrote a simple access review workflow:
     - Who: Application owners and people managers review access for their users (for example, a manager reviews their team’s access to key apps and shared mailboxes).
     - What: They check which users have access, what roles/groups they are in, and whether that access still matches each person’s job.
     - How often: Run reviews on a regular schedule (for example, quarterly for high‑risk systems and at least annually for lower‑risk apps).



### ✅ Day 5 – Identity Governance (IGA)

- Compared IAM vs IGA: Identity and Access Management (IAM) focuses on the mechanics of accounts, authentication, and authorization (who can log in and what they can do), while Identity Governance and Administration (IGA) adds the governance layer on top — approvals, policies, access reviews, and reporting to make sure access stays appropriate and compliant over time.
- Noted common IGA activities like scheduling regular access reviews, asking managers or app owners to confirm which permissions their users still need, and running SoD checks to catch unsafe combinations of access.

- Wrote a short summary of Identity Governance:
  - Identity Governance is the set of policies, processes, and tools I use to make sure the right people have the right access, that this access is approved and reviewed regularly, and that the organization can demonstrate this to auditors. It builds on IAM by adding workflows for access requests and approvals, scheduled access reviews, SoD controls, and compliance reporting so that access stays aligned with business roles and regulations over time.
