
# Step 1: Log in as Admin
open_browser("https://entra.microsoft.com")
sign_in(username="AdminAccount", password="********")

# Step 2: Identify Test User
select_user("TestUser1")  # or TestUser2

# Step 3: Navigate to Conditional Access
click_menu("Security")
click_menu("Conditional Access")
# Select existing policy or create new: "+ New Policy"

# Step 4: Configure MFA Policy
create_policy("MFA After Security Event")
assign_policy_users("TestUser1")        # Assign the test user
assign_policy_apps("All cloud apps")    # Or lab-specified app
set_policy_conditions("Security Event") # Set security event or sign-in risk
set_access_control("Grant", "Require multi-factor authentication")
enable_policy(True)
save_policy()

# Step 5: Simulate Security Event
simulate_security_event("TestUser1")  # Optional, if lab allows

# Step 6: Test MFA Enforcement
open_private_browser()
sign_in(username="TestUser1", password="********")
verify_mfa_prompt()                    # Confirm MFA is triggered

# Step 7: Verification
document_runbook("""
The test user was required to use MFA after the security event.
Conditional Access policy was applied successfully.
No administrative privileges were granted.
""")
