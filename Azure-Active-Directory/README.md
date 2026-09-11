# Azure Active Directory (Entra ID) — Identity Lifecycle Lab

This repo documents hands-on practice managing users, roles, and licenses in 
Microsoft Entra ID (Azure Active Directory), completed in my own Azure free-tier 
tenant. The exercises cover core identity lifecycle tasks — user creation, role 
assignment, bulk import, and license administration.

Exercises are structured around common identity lifecycle scenarios (user provisioning, RBAC, bulk operations, licensing) commonly covered in IAM learning paths.

## Technologies Used
- Microsoft Entra ID (Azure Active Directory)
- Microsoft 365 Admin Center
- Microsoft Graph PowerShell
- Microsoft Excel
- Role-Based Access Control (RBAC)
- Identity Lifecycle Management

## What I Practiced
- Managing users and directory roles in Entra ID
- Applying RBAC and the principle of least privilege
- Performing bulk user operations via CSV and PowerShell
- Assigning licenses and verifying usage locations
- Restoring deleted user accounts

---

## Exercise 1 — Creating and Testing a New User

**Task 1: Create a New User**
1. Signed in to the Microsoft Entra admin center as Global Administrator.
2. Navigated to Entra ID → Users → All Users → New user → Create new user.
![Signed in to Entra admin center](screenshots/Ex1-1.png)
![New user creation menu](screenshots/Ex1-2.png)
3. Set up the new account:
   - User principal name: `AlexS`
   - Display name: `Alex Smith`
   - Enabled auto-generate password
   ![New user details form filled in](screenshots/Ex1-3.png)
4. Saved the generated password securely for the next step.
5. Reviewed the details and confirmed user creation.
![Confirm Create new User ](screenshots/Ex1-4.png)
![User successfully created](screenshots/Ex1-5.png)

**Task 2: Sign In as the New User and attempt App creation**
1. Opened an incognito browser window and navigated to entra.microsoft.com.
![Incognito sign-in page](screenshots/Ex1-6.png)
2. Signed in as Alex Smith using the generated credentials.
![Signing in as Alex Smith](screenshots/Ex1-7.png)
3. Was prompted to set a new password on first login and completed that step.
![Password reset prompt](screenshots/Ex1-8.png)
4. Was prompted to set up multi-factor authentication and configured Microsoft Authenticator for the account.
![Microsoft Authenticator setup](screenshots/Ex1-9.png)
![Microsoft Authenticator setup](screenshots/Ex1-10.png)
5. Successfully signed in to the account.
![Signed in successfully](screenshots/Ex1-11.png)
6. Used the search bar to locate Enterprise Applications.
![Navigating to Enterprise Applications](screenshots/Ex1-12.png)
7. Tried to create a new application — confirmed the option was restricted, 
   as expected for a standard (non-admin) user account.
![Restricted app creation option](screenshots/Ex1-13.png)
![Restricted app creation option](screenshots/Ex1-14.png)
9. Checked the Consent and Permissions settings to verify lack of admin previleges
![Consent and permissions settings](screenshots/Ex1-15.png)
![Consent and permissions settings](screenshots/Ex1-16.png)
11. Signed out of the Alex Smith session.
![Sign-out confirmation](screenshots/Ex1-17.png)
