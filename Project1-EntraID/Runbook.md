# Project 1: Identity Foundation & Access Model
## Objective
Establish a secure identity foundation and demonstrate understanding of authentication vs authorization in Microsoft Entra ID.
---

## **Prerequisites**
1. Admin access to Microsoft Entra ID / Microsoft 365.  
2. PowerShell installed (Windows 10/11 recommended).  
3. AzureAD or AzureADPreview PowerShell module installed.  
4. Basic understanding of groups, roles, and MFA concepts.  
5. Access to Microsoft 365 Admin Center and Entra ID portal.  

---

## 1. Create Test Users

I signed in to the Microsoft Entra Admin Center and created two test users. 
The first user is testuser1@yourdomain.com with the display name Test User 1. 
The second user is testuser2@yourdomain.com with the display name Test User 2. 
Passwords were auto-generated. 
Both accounts were successfully created and are ready for testing group membership and access.

---

## 2. Create Security Groups

I created security groups called App-Access-Users and App-Access-Admins as the group type Security.
I added both test users as members.
These groups will be used to manage permissions in the lab while enforcing the principle of least privilege.

---

## 3. Enable Security Defaults (MFA)

I went to Entra ID → Properties → Manage Security Defaults and turned on Security Defaults..
This enforces multi-factor authentication (MFA) for all users, including the test accounts. 
After saving, I confirmed that when test users sign in, they are prompted to register MFA.
This ensures that even if someone knows the password, they cannot access the account without the second factor.

---

## 4. Test Sign-in as a Test User

I opened a private/incognito browser and signed in as testuser1@yourdomain.com.
After entering the email and password, I was prompted to register MFA.
I completed the registration using my phone (Authenticator app).
I verified that I could successfully access the Microsoft 365 portal after completing MFA.

---

## 5. Validate Identity Structure

1. Confirm **users exist** in Entra ID.
2. Confirm **groups exist** and have the correct members.
3. Confirm **Security Defaults / MFA** is enforced.
4. Document any issues or confirmations.

