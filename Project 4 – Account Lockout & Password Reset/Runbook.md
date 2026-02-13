# Project 4 – Account Lockout & Password Reset Runbook

## Objective
Handle a common identity support issue using a repeatable process, making sure users get back into their accounts securely while keeping everything compliant.

---

## Step 1 – Identify Locked-Out Account
I checked Microsoft Entra ID for any locked-out users and found `testuser1@yourdomain.com` showing a blocked sign-in. This lets me focus on the account that needs attention.

---

## Step 2 – Verify User Identity
Before making any changes, I confirmed the user’s identity using standard verification, like phone or email confirmation. This ensures only the right person gets access.

---

## Step 3 – Reset Password
I went into the test user’s account and reset the password. I either auto-generated a temporary password or set one manually, then made sure the user knew it securely. The account is set to require a password change at next sign-in.

---

## Step 4 – Unlock Account
If the account was blocked, I unlocked it so the user could sign in. I confirmed the sign-in status was active before moving on.

---

## Step 5 – Test Sign-In
I signed in as the test user in a private browser using the temporary password. I completed the password change and verified access to Microsoft 365. This confirms the reset and unlock worked correctly.

---

## Step 6 – Document the Process
I documented everything I did: which account was locked, how I verified identity, password reset details, unlock confirmation, and successful sign-in. This makes it easy to repeat the process for future account lockouts.

