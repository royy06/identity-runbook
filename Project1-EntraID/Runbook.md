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

1. Sign in to **Microsoft Entra Admin Center**.
2. Navigate to **Entra ID → Users → Active users**.
3. Click **New user**.
4. Fill in:
   - **User name / email**: e.g., testuser1@yourdomain.com
   - **Display name**: Test User 1
   - **Password**: Auto-generate or set manually
5. Repeat for a second test user (testuser2).
6. Save the new users.

---

## 2. Create Security Groups

1. Navigate to **Entra ID → Groups**.
2. Click **New group**.
3. Select **Security** as group type.
4. Give it a **name** (e.g., Security Test Group).
5. Add the test users as **members**.
6. Save the group.

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

