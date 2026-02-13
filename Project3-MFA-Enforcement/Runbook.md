Step 1: Log in as Admin
Open https://entra.microsoft.com


Sign in using the admin account



Step 2: Identify Test User
Select the test user for MFA enforcement


Confirm the user is active and licensed



Step 3: Navigate to Conditional Access
Click Security → Conditional Access


Select existing policy or click + New Policy



Step 4: Configure MFA Policy
Enter policy name: MFA After Security Event


Assign Users or Groups → select the test user


Assign Cloud Apps → select all or lab-specified apps


Set Conditions → security event or sign-in risk


Access Controls → Grant → Require multi-factor authentication


Enable the policy and save



Step 5: Simulate Security Event
Trigger a security event for the test user, or document the assumed event



Step 6: Test MFA Enforcement
Log in as the test user in a private browser


Attempt login to trigger the security event


Confirm MFA is prompted



Step 7: Verification
Document that:
The test user was required to use MFA after the security event. Conditional Access policy was applied successfully. No administrative privileges were granted.

