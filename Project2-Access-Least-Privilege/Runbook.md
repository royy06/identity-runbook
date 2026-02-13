# **PROJECT 2: Access Request & Least-Privilege Review**

---

## **Objective**
Simulate an access request and apply least-privilege principles.  
---

## **Prerequisites**
1. Admin access to Microsoft Entra ID / Microsoft 365.  
2. Test users created in Project 1.  
3. PowerShell installed (Windows 10/11 recommended).  
4. AzureAD or AzureADPreview PowerShell module installed.  
5. Defined allowed roles/groups for least-privilege enforcement.  

---

### **Step 1: Assign Users Using Least Privilege**
1. Navigate to **Users → All Users**.  
2. Select the user to assign to groups.  
3. Ensure only the minimum permissions required for their role are assigned.  

---

### **Step 2: Create Security Groups**
1. Navigate to **Groups → New Group**.  
2. Name the group according to role or department.  
3. Add users to the group based on their job function.  

---

### **Step 3: Review and Remove Excess Permissions**
1. Review all users’ roles and group memberships.  
2. Identify any permissions that exceed their job requirements.  
3. Remove excess roles or group memberships to enforce least privilege.  

---

### **Step 4: Review Existing Users**
1. Navigate to **Users → All Users**.  
2. Check each user’s current access and assigned groups.  
3. Document any anomalies or unnecessary access.  

---

### **Step 5: Simulate an Access Request**
1. Select a test user and simulate an access request for a group or role.  
2. Determine if the request should be approved or denied based on least privilege.  

---

### **Step 6: Validate Access**
1. Confirm the user has only the permissions allowed after the access decision.  
2. Ensure denied requests did not grant extra access.  
3. Record the final access status for each user.  

---

## **Deliverables Table Example**

| User | Action | Group | Decision | Risk Analysis | Evidence |
|------|--------|-------|----------|---------------|----------|
| User1@test.com | Assigned | SG_HR | Approved | Low – aligns with role | Document |
| User2@test.com | Removed Excess | SG_IT | Corrected | High – reduced risk | Document |
| User3@test.com | Access Request | SG_Finance | Denied | High – exceeds least privilege | Document |
