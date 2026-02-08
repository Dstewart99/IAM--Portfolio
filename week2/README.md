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

- [Project overview](Project.png)
- [Users list](Screenshot.png)
- [Review + create screen (screenshot)](Screenshot3.png)

- [Groups – create security group](Create_group.png)


