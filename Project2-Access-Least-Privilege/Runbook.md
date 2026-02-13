# **PROJECT 2: Access Request & Least-Privilege Review**

---

## **Objective
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
I added the test users to their groups.
Regular users went into App-Access-Users and admins went into App-Access-Admins.
I made sure they only got permissions required for their role — nothing extra.

---

### **Step 2: Create Security Groups**
I created two groups: App-Access-Users for regular users and App-Access-Admins for admin-level users. 
I added the test users to the appropriate groups based on what they actually need to do.
Using groups makes it easier to manage permissions without giving anyone more access than necessary.

---

### **Step 3: Review and Remove Excess Permissions**
I went through all the roles and group memberships for the test users.
If anything was over the top or unnecessary, I removed it.
This ensures no one has more access than they need, keeping things secure and clean.

---

### **Step 4: Review Existing Users**
I checked all the users in the tenant to see what access they had.
I looked for anything weird or unnecessary and documented it. 
Luckily, nothing out of the ordinary showed up, so everything looks solid.

---

### **Step 5: Simulate an Access Request**
I picked testuser1 and simulated a request to join App-Access-Admins. 
Based on the principle of least privilege, I decided this request should not be approved because the user doesn’t need admin-level access. 
For testuser2, I simulated access to App-Access-Users, which was approved since it aligns with their role. 
This shows how access requests are evaluated against actual job requirements.

---

### **Step 6: Validate Access**
After processing the access requests, I checked both users’ permissions.
testuser1 did not gain any admin access, and testuser2 only has access to the regular user group. 
All denied requests correctly blocked access, and approved requests only granted what was necessary.
The final access status for each user matches the principle of least privilege. Everything checked out with no issues.
