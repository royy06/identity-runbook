
# Step 1: Log in as Admin
open_browser("https://entra.microsoft.com")
sign_in(username="AdminAccount", password="********")
# Admin credentials only

# Step 2: Identify Test User
select_user("TestUser1")  # or TestUser2
# Ensure the test user is active and has a Microsoft 365 license

# Step 3: Navigate to Conditional Access
click_menu("Security")
click_menu("Conditional Access")
# Select an existing policy or click "+ New Policy"

# Step 4: Configure MFA Policy
create_policy("MFA After Security Event")
assign_policy_users("TestUser1")         # Assign the test user
assign_policy_apps("All cloud apps")     # Or lab-specified app
set_policy_conditions("Sign-in Risk", "High")  # Or security event
set_access_control("Grant", "Require multi-factor authentication")
enable_policy(True)
save_policy()
# MFA will trigger after defined security event; do not assign admin roles

# Step 5: Simulate Security Event
simulate_security_event("TestUser1")  # Optional if lab allows
# Or document the assumed security event

# Step 6: Test MFA Enforcement
open_private_browser()
sign_in(username="TestUser1", password="********")
verify_mfa_prompt()
# Confirm MFA is prompted

# Step 7: Verification & Documentation
document_runbook("""
The test user was required to use MFA after a security event.
Conditional Access policy "MFA After Security Event" was applied successfully.
No administrative privileges were granted.
""")
