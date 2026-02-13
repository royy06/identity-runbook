# **PROJECT 3: MFA Enforcement After Security Event**

---

## **Objective**
Demonstrate identity protection using MFA.  

---

## **Prerequisites**
1. Admin access to Microsoft Entra ID / Microsoft 365.  
2. Test users created in Project 1.  
3. Security groups created in Project 1.  
4. PowerShell installed (Windows 10/11 recommended).  
5. AzureAD or AzureADPreview module installed.  

---


### **Step 1: Simulate a Credential Risk Scenario**
The test user testuser1@tenant.onmicrosoft.com was used to simulate a credential risk scenario.
A sign-in was performed from a new browser in a private window, representing a login from an unfamiliar device. 
The sign-in location differed from previous activity. 
This created a scenario where credentials alone could allow access, demonstrating a potential security risk. 
The sign-in logs show the new device, browser, and location.

---

### **Step 2: Enforce MFA or Confirm Security Defaults**
Security Defaults were enabled in Microsoft Entra ID to enforce multi-factor authentication for the test user.
This ensures that all sign-ins now require a second factor beyond the password. 
After enabling Security Defaults, the test user was required to complete MFA via the registered phone method during sign-in. 
This change prevents unauthorized access even if credentials are compromised.



---
### **Step 3: How MFA reduces risk
Enabling multi-factor authentication reduces credential compromise by requiring an additional verification factor beyond a password.
Even if credentials are stolen, attackers cannot authenticate without the second factor. 
MFA also helps detect and block suspicious sign-ins from unfamiliar devices or locations. 
This significantly lowers the risk of unauthorized access.

---

### **Step 4: Document Login Impact
After enforcing MFA, the test user signed in using their password and was prompted for an additional verification code via the registered phone method.
Selecting “No” for “Stay signed in?” ensured the MFA prompt appeared immediately.
The login workflow now requires one extra step, slightly increasing sign-in time but greatly improving account security. 
No issues were encountered during testing, and the sign-in log confirms multi-factor authentication was successfully applied.

---

## **Deliverables Table Example**

| User | MFA Status | Security Event | Risk Mitigation | Login Impact | Evidence |
|------|------------|----------------|----------------|--------------|----------|
| User1@test.com | Enabled | Risky Login | MFA blocks unauthorized access | Login requires authenticator approval | Document |
| User2@test.com | Security Defaults Active | None | Ensures baseline protection | Standard MFA prompts | Document |

---
