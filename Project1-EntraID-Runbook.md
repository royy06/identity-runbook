# Project 1: Identity Foundation & Access Model

## Objective
Establish a secure identity foundation and demonstrate understanding of authentication vs authorization in Microsoft Entra ID.

---

## 1. Test Users Created

| User Email             | Display Name      | Password (Test Only) | Group Assignment       | MFA / Security Defaults |
|------------------------|-----------------|-------------------|----------------------|-----------------------|
| testuser1@domain.com    | Test User 1     | Test1234!          | Security Test Group   | Enabled               |
| testuser2@domain.com    | Test User 2     | Test1234!          | Security Test Group   | Enabled               |

**Screenshots:**
- `screenshots/Project1-EntraID/Users_List.png`

---

## 2. Security Groups Created

| Group Name              | Members                   | Purpose                         |
|-------------------------|---------------------------|--------------------------------|
| Security Test Group      | testuser1, testuser2      | Apply MFA/Security Defaults     |

**Screenshots:**
- `screenshots/Project1-EntraID/Groups_List.png`

---

## 3. Multi-Factor Authentication (MFA)

**Configuration:**  
- Enabled via **Security Defaults** for all users in the group.  
- MFA enforced at first login.

**Test Steps:**
1. Open **Microsoft 365 portal** in an incognito browser.
2. Sign in as `testuser1@domain.com` with password.
3. MFA setup prompt appears (Authenticator app / QR code).

**Screenshots:**
- `screenshots/Project1-EntraID/MFA_QR.png`
- `screenshots/Project1-EntraID/MFA_Login.png`

---

## 4. Conditional Access (if applicable)

**Policy Applied:**
- Target Users/Groups: Security Test Group  
- Grant: Require MFA  
- Cloud Apps: All  

**Test Steps:**
1. Sign in with test user from a new device or network.  
2. Verify that access is blocked or MFA prompted according to policy.

**Screenshots:**  
- (Add here if Conditional Access was tested)

---

## 5. Identity Structure Validation

**Steps:**
1. Confirm users exist and are assigned to correct groups.  
2. Confirm MFA or Security Defaults are enforced.  
3. Test login for each test user.  

**Screenshots:**  
- `screenshots/Project1-EntraID/Users_List.png`  
- `screenshots/Project1-EntraID/Groups_List.png`  
- `screenshots/Project1-EntraID/MFA_QR.png`  
- `screenshots/Project1-EntraID/MFA_Login.png`

---

**Notes / Lessons Learned:**
- MFA/Security Defaults enforce identity protection for all users.  
- Test users allow safe validation of policies without risking real accounts.
