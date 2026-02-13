# Project 5: Identity Governance & JML Lifecycle

-

**Objective:**  
Manage the identity lifecycle for users — Joiner, Mover, Leaver — and ensure access follows governance policies.  
-
##**Prerequisites:** 

- Access to Microsoft Entra Admin Center  
- Two test user accounts (TestUser1 and TestUser2)  
- Security groups: App-Access-Users and App-Access-Admins  
- Basic understanding of JML lifecycle (Joiner, Mover, Leaver)  
- Access to Identity Governance / Access Reviews  

---

## Step 1 – Create Test Users (Joiner)

I created TestUser1 and TestUser2 to simulate adding new employees.  

---

## Step 2 – Assign Roles / Groups (Mover)

I moved TestUser2 from App-Access-Users to App-Access-Admins to simulate a role change and ensure proper access.  

---

## Step 3 – Remove Access (Leaver)

I removed TestUser1’s access from all groups to simulate an employee leaving the company.  

---

## Step 4 – Conduct Access Review / Governance Check

I ran an access review to make sure users only had the access they needed.  

---

## Step 5 – Document Findings

I confirmed TestUser2 had correct access after the move, and TestUser1’s access was removed as expected. 
