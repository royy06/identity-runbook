
# objective:
# enforce multi-factor authentication (mfa) for a test user after a security event
# demonstrate conditional access and least privilege

# prerequisites:
# admin account for microsoft entra id
# test user from previous projects (testuser1 or testuser2)
# microsoft 365 license assigned
# browser: normal mode for admin, private/incognito for test user

# step 1: log in as admin
open_browser("https://entra.microsoft.com")
sign_in("adminaccount", "********")

# step 2: identify test user
search_user("testuser1")  # or testuser2
select_user("testuser1")

# step 3: navigate to conditional access
click_menu("security")
click_menu("conditional access")
# select existing policy or create "+ new policy"

# step 4: create/configure mfa policy
click_button("new policy")
enter_text("policy name", "mfa after security event")
click_section("assignments → users or groups")
select_user("testuser1")
click_section("assignments → cloud apps")
select_option("all cloud apps")  # or lab-specified
click_section("conditions")
select_option("sign-in risk", "high")  # or security event
click_section("access controls → grant")
select_option("require multi-factor authentication")
toggle_switch("enable policy", true)
click_button("save policy")

# step 5: simulate security event
simulate_sign_in_event("testuser1", "high")  # optional if lab allows

# step 6: test mfa enforcement
open_private_browser()
navigate_to("office.com")
sign_in("testuser1", "********")
verify_mfa_prompt()

# step 7: verification & documentation
document_runbook("""
test user was required to use mfa after a security event.
conditional access policy 'mfa after security event' was applied successfully.
login verification confirmed mfa prompt.
no administrative privileges were granted.

