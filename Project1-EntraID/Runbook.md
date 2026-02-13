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

I created a security group called App-Access-Users as the group type Security.
I added both test users as members.
This group will be used to manage permissions in the lab while enforcing the principle of least privilege.

---

## 3. Enable Security Defaults (MFA)

1. Go to **Entra ID → Properties → Manage Security Defaults**.
2. Turn **Enable Security Defaults** to **Yes**.
3. Save the settings.
4. Verify the test users are affected:
   - When they sign in, they should be prompted to **register MFA**.

---

## 4. Test Sign-in as a Test User

1. Open a **private/incognito browser**.
2. Go to **Microsoft 365 portal**.
3. Sign in with a test user account:
   - Enter **email** and **password**.
4. Complete **MFA registration** (phone or Authenticator app).
5. Verify you can successfully access the portal after MFA.

---

## 5. Validate Identity Structure

1. Confirm **users exist** in Entra ID.
2. Confirm **groups exist** and have the correct members.
3. Confirm **Security Defaults / MFA** is enforced.
4. Document any issues or confirmations.

