# Week 2 – Entra ID Labs


## Day 6 focuses on creating internal users and security groups that I’ll use later for Conditional Access and PIM labs.

**Task: Create a new internal user in Microsoft Entra ID**

- Navigated to **Microsoft Entra admin center → Users → All users → + New user → Create new user**.
- Entered core identity details:
  - User principal name: Zjohnson
  - Display name: Zack Johnson 
  - Left the mail nickname as the default.

- Opened the **Properties** tab and set:
  - First name: `Zack`
  - Last name: `Johnson`
  - User type: **Member** (internal employee; Guest would be used for external collaborators and has more restricted capabilities).
  - Usage location: `United States`.
- Selected **Review + create → Create** to provision the new internal user account.






- Created a security group named `IAM-Test-Employees` in **Entra ID → Groups → All groups → New group** with type **Security** and assigned membership.
- Added the new internal user (`Zjohnson`) as a member of this group to use later for group-based access assignments and Conditional Access tests.

### 📸 Day 6 Screenshots

- [Create user screen (screenshot)](Project.png)

- [Users list](Screenshot.png)
- [Review + create screen (screenshot)](Screenshot3.png)

- [Groups – create security group](Create_group.png)


## Day 7 – Conditional Access

Day 7 focuses on using Conditional Access to require MFA when employees access a sensitive Microsoft service.

**Task: Require MFA for IAM-Test-Employees when accessing Microsoft Service Trust**

- Reviewed Conditional Access as Entra ID’s policy engine that evaluates signals (user, app, device, location, risk) and then decides whether to allow, block, or require extra controls like MFA.
- Created policy **CA-Require-MFA-Employees** in **Protection → Conditional Access → New policy** and targeted the `IAM-Test-Employees` security group under **Users or agents (Preview) → Specific users included → Select users and groups**.
- Selected **Microsoft Service Trust** as the cloud app under **Target resources → Select resources → Select specific resources**, so the policy protects access to that compliance/security portal.
- Left advanced conditions (sign-in risk, user risk, device platforms, locations) not configured for this initial lab to keep the policy focused purely on MFA enforcement.
- Under **Access controls → Grant**, chose **Grant access** and enabled **Require multi-factor authentication**, then turned the policy **On** and created it.
- Documented the policy behavior in plain language:  
  “When any user in the `IAM-Test-Employees` group signs in to Microsoft Service Trust, they must complete MFA. If MFA fails, access to the portal is blocked.”

### 📸 Day 7 Screenshots

- [Policy targeting IAM-Test-Employees group (screenshot)](IAM-Test-Employees.png)
- [Microsoft Service Trust selected as target app (screenshot)](Target_app.png)
- [Grant controls requiring MFA (screenshot)](Grant.png)



-----------------------------------------------------------

### Day 8 – Privileged Identity Management (PIM)
**Just-in-time access vs standing admin access**

- Just-in-time access: Admin roles are assigned as eligible and only activated for a limited time when needed, often with MFA, justification, or approval.  
- Standing admin access: Admin roles are permanently active, so elevated permissions are always on and available to the account.  

**Eligible vs active roles**

- Eligible role: The user can request activation of the role when they need it, but does not have the admin permissions until it is activated.  
- Active role: The user already has the role’s permissions without any activation step and can use them immediately. 

Day 8 focuses on using Microsoft Entra Privileged Identity Management to replace standing admin access with just‑in‑time elevation for sensitive roles.

- Reviewed how PIM provides **just‑in‑time** admin access so elevated permissions are only active when needed instead of being permanently assigned. 
- Learned the difference between eligible assignments (can be activated on demand) and active assignments (admin rights already on without any activation step). 

**Steps – Make Security Reader eligible in PIM**

1. In the Microsoft Entra admin center, go to **Identity Governance → Privileged Identity Management → Microsoft Entra roles**. 
2. Select **Roles**, search for **Security Reader**, and open the role. 
3. Click **Assignments → Add assignments**. 
4. Under **Select members**, choose my Dee Secure admin account and click **Next**. 
5. On the **Settings** tab, set **Assignment type = Eligible** and leave it permanently eligible for this lab, then click **Assign**.

**Steps – Activate the eligible role (just‑in‑time)**

1. Go to **Privileged Identity Management → My roles**. 
2. On the **Eligible assignments** tab, find **Security Reader** and click **Activate**. 
3. Choose a short **duration**, enter a reason like “Day 8 PIM lab – test JIT access,” and complete MFA if prompted. 
4. Click **Activate**, then verify Security Reader appears on the **Active assignments** tab with the option to **Deactivate**. 
5. (Optional) Click **Deactivate** when finished to remove the elevated Security Reader access before the end time. 


### Day 8 Screenshots

- [PIM – Security Reader eligible assignment (screenshot)](Security_Reader.png)
- [PIM – Security Reader active assignment (screenshot)](Active.png)
--------

### Day 9 – Entra Roles with Role-Assignable Groups

Focuses on assigning Microsoft Entra admin roles through a role-assignable group instead of directly to a user, so access is easier to manage and audit.

**Goal:** Use a security group to grant the User Administrator role to members, then verify that membership controls who has that admin access.

**Steps – Create a role-assignable group**

1. In the Microsoft Entra admin center, go to **Identity → Groups → All groups → New group**.
2. Set **Group type = Security**, name it `IAM-User-Admins`, and add a description like “Role-assignable group for User Administrator lab.”
3. Turn **Microsoft Entra roles can be assigned to the group** to **Yes**.
4. Under **Members**, add my test user account to the `IAM-User-Admins` group before clicking **Create**.
5. Click **Create** to finish creating the role-assignable group with my test user already as a member.
6. In **Identity → Users → [that test user] → Assigned roles**, verify that the user now has **User Administrator** via the group.  


**What I learned**

- Admin roles like User Administrator can be assigned directly to users or to role-assignable groups.  
- Using a group (such as `IAM-User-Admins`) makes it easier for an IAM analyst to grant and remove admin access by changing group membership instead of editing role assignments on each user.  
- This pattern lines up with least privilege and governance: the group represents an approved admin responsibility, and only members of that group receive the User Administrator role.


### Day 9 Screenshots

- [IAM-User-Admins role-assignable group (screenshot)](Groups.png)
- [User Administrator assigned to IAM-User-Admins group (screenshot)](IAM-User-Admins.png)
- [Test user showing inherited User Administrator role (screenshot)](proof-user-added.png)

----
## Day 10 – Exercise: Perform basic Self-Service Password Reset (SSPR) tasks

In this exercise I learned where the self-service password reset (SSPR) feature is configured in Microsoft Entra and walked through enabling it for a specific group. 

### Task 1 – View and configure SSPR properties for a group

- Opened the **Microsoft Entra admin center** and went to  Password reset → Properties**. 
- Reviewed the **Self service password reset enabled** options: **None** (no users), **Selected** (only selected groups), and **All** (all users). 
- Set the value to **Selected**, chose my lab group (IAM-Test-Employees), and saved the configuration so only this group can use SSPR. - [SSPR properties for test group (screenshot)](SSPR_IAM-Test-Employees_properties.png.png)

### Subtask 2 – Configure SSPR authentication methods

- From **Password reset → Authentication methods**, set **Number of methods required to reset** to **1**, meaning users must verify with one authentication method before they can reset their password (the password itself does not count as a method). 
- Selected **Email**, **Mobile phone**, and **Mobile app code** as the **Methods available to users** so they have multiple options for verification. 
- Saved the configuration, completing the basic setup of authentication methods for SSPR. [SSPR Autentication – user and admin email alerts (screenshot)](SSPR.png)


### Subtask 3 – Configure SSPR registration

- Opened **Password reset → Registration**. 
- Verified **Require users to register when signing in?** was set to **Yes** so users are prompted to register their SSPR methods during sign-in. 
- Set **Number of days before users are asked to re-confirm their authentication information** to **90** days and saved the settings to keep registration data up to date. [SSPR registration – users re-confirm every 90 days (screenshot)](90days.png)



### Subtask 4 – Configure SSPR reset notifications

- Went to **Password reset → Notifications**. 
- Left **Notify users on password reset?** at the default value of **Yes** so users receive an email when their password is reset through SSPR. 
- Changed **Notify all admins when other admins reset their password?** to **Yes**, then saved the configuration to increase visibility into privileged password reset activity. [SSPR notifications – user and admin email alerts (screenshot)](Notification.png)



----

## Day 11 – Perform basic Password Protection tasks

In this exercise I explored the Microsoft Entra ID password protection capabilities used to enforce stronger passwords and reduce password attack risk. [page:0][web:129]

### Task 1 – View lock settings, duration, and threshold values

- Opened the **Microsoft Entra admin center** at `https://entra.microsoft.com` and signed in with my lab tenant account.
- From the left menu, went to **Entra ID → Authentication methods** and selected **Password protection**. 

- Enabled **Custom smart lockout** with:
  - **Lockout threshold** set to **5**, so the account locks after five failed password attempts.  
  - **Lockout duration** set to **30 seconds**, defining how long the account remains locked when the threshold is reached. 

- Turned on **Enforce custom list** and added the following custom banned password terms to block weak, organization-specific passwords:
  - `Contoso`  
  - `London`  
  - `Widget`  

  This simulates a company named Contoso in London that makes widgets, ensuring those words cannot be part of a user’s password.

- Set **Mode** to **Enforced** and selected **Save** so the custom banned password list and smart lockout settings actively apply to sign-ins and password changes.

[Password protection – smart lockout and custom banned password list (screenshot)](Password_protection.png)







