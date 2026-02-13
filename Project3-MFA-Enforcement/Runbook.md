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
1. Identify a test user account to simulate a security event (e.g., risky login).  
2. Document the scenario details, such as login location, device, or sign-in risk.  

---

### **Step 2: Enforce MFA or Confirm Security Defaults**
1. Navigate to **Users → All Users** in Microsoft Entra ID.  
2. Enable MFA for the test user(s) or confirm that Security Defaults are active.  
3. Optionally, assign Conditional Access policy enforcing MFA for specific groups.  

---

Enabling multi-factor authentication reduces credential compromise by requiring an additional verification factor beyond a password.
Even if credentials are stolen, attackers cannot authenticate without the second factor. 
MFA also helps detect and block suspicious sign-ins from unfamiliar devices or locations. 
This significantly lowers the risk of unauthorized access.

---

### **Step 4: Document Login Impact**
1. Test sign-in for the MFA-enabled account.  
2. Record login workflow changes and user experience.  
3. Include a summary of any issues or successes.  

---

## **Deliverables Table Example**

| User | MFA Status | Security Event | Risk Mitigation | Login Impact | Evidence |
|------|------------|----------------|----------------|--------------|----------|
| User1@test.com | Enabled | Risky Login | MFA blocks unauthorized access | Login requires authenticator approval | Document |
| User2@test.com | Security Defaults Active | None | Ensures baseline protection | Standard MFA prompts | Document |

---

