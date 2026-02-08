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

