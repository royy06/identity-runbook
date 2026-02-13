# Step 1: Log in as Admin
open_browser("https://entra.microsoft.com")
sign_in(username="AdminAccount", password="********")  # Use admin credentials
# NOTE: Only admin can create or modify Conditional Access policies
# Screenshot: Admin dashboard showing login

# Step 2: Identify Test User
select_user("TestUser1")  # or TestUser2
# NOTE: Ensure the user has a Microsoft 365 license and is active

# Step 3: Navigate to Conditional Access
click_menu("Security")
click_menu("Conditional Access")
# If lab provides a pre-existing policy, select it
# Otherwise: click "+ New Policy"
# Screenshot: Conditional Access policies page

# Step 4: Configure MFA Policy
create_policy("MFA After Security Event")
assign_policy_users("TestUser1")   # Assign the test user
assign_policy_apps("All cloud apps") # Or lab-specified app
set_policy_conditions("Sign-in Risk", "High")  # If lab requires
set_access_control("Grant", "Require multi-factor authentication")
enable_policy(True)
save_policy()
# NOTES:
# - MFA triggers after defined security event
# - Do NOT assign admin roles
# Screenshot: Policy settings page showing user assignment and MFA requirement

# Step 5: Simulate Security Event
# If lab allows, simulate risky sign-in
# Otherwise, document the assumed security event
simulate_security_event("TestUser1")  # Optional
# Screenshot: Optional placeholder for simulation

# Step 6: Test MFA Enforcement
open_private_browser()
sign_in(username="TestUser1", password="********")  # Use test user credentials
# Attempt login that triggers security event
verify_mfa_prompt()
# Screenshot: MFA prompt screen

# Step 7: Verification & Documentation
document_runbook("""
The test user was identified for MFA enforcement after a security event. 
Conditional Access policy “MFA After Security Event” was applied, requiring multi-factor authentication. 
Login was successfully verified to prompt MFA. 
No administrative privileges were granted.
""")
