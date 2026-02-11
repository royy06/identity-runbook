# Project 1 – Identity Foundation & Access Model

## Objective
Establish a basic identity foundation by creating users, security groups, and enforcing authentication controls. This project demonstrates the difference between authentication and authorization.

---

## Scope
- User identity creation
- Group-based access control
- MFA enforcement
- Basic identity documentation

---

## Tools Used
- Microsoft Entra ID (Azure Active Directory)
- Azure Portal

---

## Pre-Requisites
- Tenant access with Global Administrator or Identity Administrator role
- Test environment (non-production)

---

## Step-by-Step Actions

### Step 1: Create Test Users
1. Navigate to **Entra ID → Users**
2. Create two test users:
   - `testuser1`
   - `testuser2`
3. Assign temporary passwords and require password change at first login

**Purpose:**  
Represents individual identities within the directory.

---

### Step 2: Create Security Groups
1. Navigate to **Entra ID → Groups**
2. Create two security groups:
   - `SG_HR`
   - `SG_IT`
3. Set group type to **Security**

**Purpose:**  
Used to manage authorization through group-based access.

---

### Step 3: Assign Users to Groups
- Add `testuser1` to `SG_HR`
- Add `testuser2` to `SG_IT`

**Purpose:**  
Demonstrates authorization by granting access through group membership.

---

### Step 4: Enable MFA / Security Defaults
1. Navigate to **Entra ID → Properties**
2. Enable **Security Defaults** OR
3. Enforce MFA for test users

**Purpose:**  
Strengthens authentication security.

---

### Step 5: Validate Identity Structure
- Confirm users can sign in
- Verify group membership
- Ensure MFA prompt appears on login

---

## Authentication vs Authorization

- **Authentication:** Verifying who the user is (username, password, MFA)
- **Authorization:** Determining what the user can access (group membership)

This project demonstrates both concepts using Entra ID users and security groups.

---

## Screenshot Evidence
![Project 1 Screenshot](../Screenshots/Project1.png)

---

## Outcome
- Identity foundation successfully established
- Group-based access model implemented
- MFA enforced for improved security posture

