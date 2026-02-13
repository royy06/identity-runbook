1. Purpose
Enforce Multi-Factor Authentication (MFA) for test users and monitor security events in Microsoft Entra ID.

2. Prerequisites
Admin access to Microsoft Entra ID / Microsoft 365


Two test users created in Project 1


Two security groups from Project 1 (e.g., SG_HR, SG_IT)



3. Procedure
Step 1: Access Entra ID
Sign in to Microsoft 365 Admin Center.


Click Show all → Entra ID.


Verify you are in the Entra ID portal.



Step 2: Enable MFA for Users
Navigate to Users → All Users.


Select the test users.


Click Authentication methods → Require MFA.


Confirm status shows Enabled / Enforced.


Take screenshots of each user’s MFA status.



Step 3: Apply Conditional Access Policy
Navigate to Security → Conditional Access → New Policy.


Name the policy: MFA Enforcement – Project 3.


Assign Users or Groups (SG_HR, SG_IT).


Under Grant → Require multi-factor authentication, select Require MFA.


Enable the policy and click Save.


Take a screenshot of the policy assignment.



Step 4: Monitor Security Events
Navigate to Security → Audit logs.


Filter for Sign-in events and MFA activity.


Review for:


Failed sign-ins


MFA registration completion


Policy application


Take screenshots of relevant events.



Step 5: Document Outputs
Save screenshots in folder: Project3_MFA_Events.


Create a table for MFA enforcement evidence:
