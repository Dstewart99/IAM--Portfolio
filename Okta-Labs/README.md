# Lab 01 – Add Users Manually in Okta OIE

## Objective
Practice manually creating a user in Okta Identity Engine (OIE) via the Admin Console.

## Environment
- Okta Integrator Org (OIE)
- Admin Console → Directory → People

## Exam Relevance
- User lifecycle management
- Understanding activation methods and resulting user states

---

## Steps

### 1. Navigate to Directory → People
- In the Admin Console, go to **Directory > People**
- Click **Add Person**

### 2. Fill Out the Add Person Form

| Field | Value Used |
|---|---|
| User Type | User (default) |
| First Name | Dee |
| Last Name | Job |
| Username | deejob101@gmail.com |
| Primary Email | deejob101@gmail.com |
| Secondary Email | *(left blank)* |
| Groups | *(left blank)* |
| Activation | Activate now |
| I will set password | *(unchecked — Okta sends activation email)* |

### 3. Save the User
- Click **Save**
- Okta sends an activation email to the primary email address

---

## Screenshots

**Add Person form filled out:**
- [Add Person Form](create_profile.png)

**Activation email received:**
- [Add Person Form](Activation_email.png)

**User status after activation:**
- [Add Person Form](User_Status.png)



---

## Key Concepts

| Activation Method | Resulting User State |
|---|---|
| Activate now (no password set) | Pending Activation → Active (after email click) |
| Activate now (password set by admin) | Active immediately |
| Activate later | Staged |

## Notes
- Username must be in email format
- "User must change password on first login" appears only when admin sets the password
- Staged users receive no email and cannot log in until activated
- -------
# Lab 02 – Deactivate and Delete User Accounts in Okta OIE

## Objective
Practice deactivating and deleting a user account in Okta Identity Engine (OIE) via the Admin Console.

## Environment
- Okta Integrator Org (OIE)
- Admin Console → Directory → People

## Exam Relevance
- User lifecycle management
- Understanding the difference between suspended, deactivated, and deleted states

---

## Key Concepts

| Action | User Loses App Access | Admin Roles Revoked | Factors Removed | Removed from Groups | Permanent |
|---|---|---|---|---|---|
| Suspended | No | No | No | No | No |
| Deactivated | Yes | Yes | No | No | No |
| Deleted | Yes | Yes | Yes | Yes | Yes |

> Note: A user must be deactivated before they can be deleted. Deletion cannot be undone.

---

## Steps

### Part 1 – Deactivate a User

1. In the Admin Console, go to **Directory > People**
2. Select the user account to deactivate
3. Click **More Actions → Deactivate**
4. Click **Deactivate** in the confirmation dialog
5. User status changes from **Active → Deactivated**

### Part 2 – Delete a User

1. In the Admin Console, go to **Directory > People**
2. Search for the deactivated user
3. Click the username to open their profile
4. Click **Delete**
5. Click **Delete** in the confirmation dialog to permanently remove the account

---

## Screenshots
- [User Active Status Before Deactivation](deactivate-before.png)
- [Deactivation Confirmation Dialog](deactivate-confirm.png)
- [User Deactivated Status](deactivate-after.png)
- [Delete Confirmation Dialog](delete-confirm.png)

---

## Notes
- Deactivated users are removed from app access but remain in all Okta groups
- Deleted users have their username freed up for reuse
- Okta permanently deletes customer data within 30 days of account deletion
- Admins receive an email listing all users deactivated in the past 30 minutes


