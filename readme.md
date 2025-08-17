# Microsoft 365 + Entra ID User Lifecycle Lab Workflow

This lab demonstrates **onboarding, managing, and offboarding employees** in Microsoft 365 and Entra ID (Azure AD).

---

## 1️⃣ Set up Microsoft 365 Tenant
- Go to Microsoft 365 Business Basic/Standard trial → Try free for 1 month.
- Create tenant with custom domain (e.g., yourname.onmicrosoft.com).
- Set global admin credentials and log in at Admin Center.

![Admin Center Dashboard](screenshots/01_AdminDashboard.png)

---

## 2️⃣ Access Entra ID (Azure AD)
- Go to [entra.microsoft.com](https://entra.microsoft.com)
- Explore **Users** and **Groups** sections.

![Entra ID Overview](screenshots/02_EntraOverview.png)

---

## 3️⃣ Create a New User
- Entra ID → Users → New user → Fill details:
  - Name: John Doe
  - Username: johndoe@yourtenant.onmicrosoft.com
  - Password: Auto-generate
  - Assign Microsoft 365 Business Basic license → Save

![New User Form](screenshots/03_NewUserForm.png)
![User List](screenshots/04_UserList.png)

---

## 4️⃣ Assign Group Membership
- Groups → New group → Sales Team → Add John Doe

![Group Creation Form](screenshots/05_GroupCreation.png)
![Total Groups](screenshots/05.1_GroupTotal.png)

---

## 5️⃣ Simulate First Login
- Open Incognito → Login as John Doe → Change password
- Access Outlook to verify mailbox

![First Login Password Change](screenshots/06_FirstLogin.png)
![Outlook Inbox](screenshots/07_OutlookInbox.png)

---

## 6️⃣ Reset Password
- Admin → Users → John Doe → Reset password

![Password Reset Confirmation](screenshots/08_PasswordReset.png)

---

## 7️⃣ Block & Unblock Sign-in
-Admin Center → Users → Test account → Block sign-in → check → save
-Admin Center → Users → Test account → unblock sign-in → uncheck → save

![Account Status Blocked](screenshots/09_block_sign-in.png)
![Account Status Blocked](screenshots/09.1_blocked_user.png)
![Account Status Blocked](screenshots/09.2_unblock_sign-in.png)

---

## 8️⃣ Remove License & Delete User
- John Doe → Licenses → Unassign → Delete

![User Deletion Confirmation](screenshots/10_liscense_removing.png)
![User Deletion Confirmation](screenshots/10.1_UserDeletion.png)

---

## 9️⃣ Restore Deleted User
- Deleted Users → Select John Doe → Restore

![Restored User](screenshots/11_RestoredUser.png)

---

## 🔹 10️⃣ Create Azure AD Groups for Departments
- Groups → New group → HR Department → Add members manually
- Repeat for IT Department and Finance Department

![Groups List](screenshots/13_GroupsList.png)

---

## 🔹 11️⃣ Assign Users to Groups
- Add users manually to HR, IT, Finance groups

![Users in Groups](screenshots/22_UsersAddedToGroups.png)

---

## 🔹 12️⃣ Configure MFA
- Admin Center → Users → Active Users → Manage multifactor authentication → Enable

![MFA Enabled](screenshots/16_MFAEnabled.png)

---

## 🔹 13️⃣ Log in as User & Complete MFA Setup
- Incognito → John Doe → Set up Authenticator/SMS

![MFA Setup](screenshots/17_MFASetup.png)
![Successful MFA Login](screenshots/18_MFALogin.png)

---

## 🔹 14️⃣ Bulk User Creation
- Users → Bulk create → Upload CSV → Assign licenses

![CSV Upload](screenshots/19_CSVUpload.png)

---

## 🔹 15️⃣ Assign Licenses & Groups
- Users → Active Users → Select multiple → Assign license
- Groups → Add members manually

![Multiple Users Licensed](screenshots/21_MultipleLicenses.png)
![Users Added to Groups](screenshots/22_UsersAddedToGroups.png)

---

## 🔹 16️⃣ Password Reset Simulation
- Users → John Doe → Reset password
- Audit Logs → Verify event recorded

![Password Reset Confirmation](screenshots/08_PasswordReset.png)
![Audit Log Entry](screenshots/24_AuditLog.png)

---

## 🔹 17️⃣ Simulate Offboarding Process
### Disable Sign-In
- Entra ID → John Doe → Block sign-in = Yes

![Account Blocked](screenshots/09_block_sign-in.png)

### Remove from All Groups
- Groups → Remove John Doe from HR/IT/Finance

![Group Membership Empty](screenshots/26_GroupsEmpty.png)

### Remove Licenses and deleting user
- John Doe → Licenses → Unassign

![Licenses Removed](screenshots/27_LicensesRemoved.png)
![Licenses Removed](screenshots/28_deleting_user.png)


---

