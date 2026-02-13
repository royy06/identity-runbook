
# Step 1: Log in as Admin
open_browser("https://entra.microsoft.com")
sign_in(username="AdminAccount", password="********")
# Wait for dashboard to load

# Step 2: Identify Test User
click_menu("Users")
search_user("TestUser1")  # or TestUser2
select_user("TestUser1")
# Confirm user is active and has a Microsoft 365 license

# Step 3: Navigate to Conditional Access
click_menu("Security")
click_menu("Conditional Access")
# If existing policy exists, select it
# Otherwise, click "+ New Policy"

# Step 4: Create/Configure MFA Policy
click_button("New Policy")               # If creating new
enter_text("Policy Name", "MFA After Security Event")
click_section("Assignments → Users or Groups")
select_user("TestUser1")
click_section("Assignments → Cloud Apps")
select_option("All cloud apps")          # Or lab-specified app
click_section("Conditions")
select_option("Sign-in Risk", "High")   # Or security event per lab
click_section("Access Controls → Grant")
select_option("Require multi-factor authentication")
toggle_switch("Enable Policy", True)
click_button("Save Policy")
# Policy is now active

# Step 5: Simulate Security Event
# Optional if lab allows
simulate_sign_in_event("TestUser1", risk="High")
# Or document assumed security event

# Step 6: Test MFA Enforcement
open_private_browser()
navigate_to("office.com")
sign_in(username="TestUser1", password="********")
# Attempt login to trigger security event
verify_mfa_prompt()                      # Confirm MFA is prompted

# Step 7: Verification & Documentation
document_runbook("""
The test user was required to use MFA after a security event.
Conditional Access policy 'MFA After Security Event' was applied successfully.
Login verification confirmed MFA prompt.
No administrative privileges were granted.
""")
