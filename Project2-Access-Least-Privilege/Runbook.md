# **Project 2 Runbook – Access Request & Least Privilege Review**
---
## **Objective**
- Review user access requests and group memberships.  
- Apply the principle of least privilege to ensure users have only the permissions required for their roles.  
- Document findings for compliance and security auditing.  

---

## **Prerequisites**
1. Admin access to Microsoft Entra ID / Microsoft 365.  
2. Test users and security groups created in Project 1.  
3. PowerShell installed (Windows 10/11 recommended).  
4. AzureAD or AzureADPreview PowerShell module installed.  
5. Defined allowed roles for least privilege enforcement (e.g., User, Guest, Member).  

---

## **Procedure**

### **Step 1: Access Microsoft Entra ID**
1. Sign in to **Microsoft 365 Admin Center**.  
2. Click **Show all → Entra ID**.  
3. Verify you are in the **Entra ID portal**.  

---

### **Step 2: Review User Access**
1. Navigate to **Users → Access Reviews / Access Requests**.  
2. Select each test user for review.  
3. Check group memberships and assigned roles.  
4. Take screenshots of current access for documentation.  

---

### **Step 3: Apply Least Privilege**
1. Remove any unnecessary roles or permissions.  
2. Ensure users only have permissions required for their job.  
3. Take screenshots of updated permissions.  

---

### **Step 4: Approve or Deny Access Requests**
1. Navigate to **pending access requests**.  
2. Approve requests that meet least privilege standards.  
3. Deny requests that grant excessive permissions.  
4. Take screenshots of approvals/denials.  

---

### **Step 5: Document Outputs**
1. Save all screenshots in a folder named `Project2_Access_LeastPrivilege`.  
2. Create a summary table of your review:

| User | Group | Role | Access Status | Least Privilege Applied |
|------|-------|------|---------------|------------------------|
| User1@test.com | SG_HR | Member | Approved | ✅ |
| User2@test.com | SG_IT | Owner | Denied | ✅ |

---

### **GitHub Repo Structure (Recommended)**
