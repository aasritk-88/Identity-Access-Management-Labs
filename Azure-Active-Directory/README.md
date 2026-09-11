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

I signed into the Microsoft Entra admin center as Global Administrator and 
created a new test user, Alex Smith, via Users → All Users → New user, with 
auto-generated password enabled.

To verify the account was correctly provisioned, I opened an incognito browser 
session and signed in as Alex Smith, updating the temporary password on first 
login. From there, I checked Enterprise Applications to confirm the account 
had standard user privileges rather than admin rights — the "Create your own 
application" option was unavailable, as expected for a non-admin account. I also 
looked through the Consent and Permissions settings to see what a standard 
user can and can't access by default.
