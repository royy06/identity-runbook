# Project 2: Access Requests & Least Privilege Review

## Objective
Demonstrate the principle of least privilege by managing access through security groups and validating that users only have the permissions required for their role.

---

## Prerequisites
- Microsoft Entra ID tenant
- At least two test users
- Admin access to Entra ID

---

## Step 1: Review Existing Users

1. Sign in to the Microsoft Entra Admin Center.
2. Navigate to **Entra ID → Users → Active users**.
3. Verify that at least two test users exist.
4. Confirm that users do not have unnecessary roles or permissions assigned.

---

## Step 2: Create Security Groups

1. Navigate to **Entra ID → Groups**.
2. Select **New group**.
3. Configure the group:
   - Group type: Security
   - Group name: App-Access-Users
   - Membership type: Assigned
4. Create the group.
5. Repeat the process to create:
   - Group name: App-Access-Admins

---

## Step 3: Assign Users Using Least Privilege

1. Open the **App-Access-Users** group.
2. Add **one test user only**.
3. Do not assign users to the Admin group unless required.
4. Leave the second test user without group access.

---

## Step 4: Simulate an Access Request

1. Identify the test user without group access.
2. Assume the user requests access to application resources.
3. Review the request to confirm business need.
4. Approve the request by adding the user to:
   - App-Access-Users group
5. Do not grant admin-level access.

---

## Step 5: Validate Access

1. Sign in as the approved test user.
2. Confirm access is available.
3. Sign in as the unapproved test user.
4. Confirm access is restricted or unavailable.

---

## Step 6: Review and Remove Excess Permissions

1. Navigate to **Entra ID → Groups**.
2. Review all group memberships.
3. Remove any users with unnecessary access.
4. Confirm no users have admin privileges without justification.

---

## Step 7: Access Review Confirmation

1. Verify all access is granted through groups.
2. Confirm least privilege is enforced.
3. Ensure access assignments match user roles.

