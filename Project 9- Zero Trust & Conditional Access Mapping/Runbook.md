# Project 9: Zero Trust & Conditional Access Mapping

## Objective
Map identity and access controls to Zero Trust principles to demonstrate how access is continuously verified and protected.

## Prerequisites
- Basic understanding of Zero Trust concepts
- Access to Microsoft Entra ID (or knowledge of its features)
- Familiarity with MFA, Conditional Access, and security groups
- Test users and groups (App-Access-Users, App-Access-Admins)

---

## Step 1 – Identify Zero Trust Principles

I reviewed the core Zero Trust principles and focused on:
- Verify explicitly
- Use least privilege access
- Assume breach

I used these principles as the baseline for mapping identity controls.

---

## Step 2 – Map Identity Controls to Zero Trust

I mapped common identity controls in Entra ID to each Zero Trust principle:

### Verify Explicitly
- Multi-Factor Authentication (MFA)
- Conditional Access policies
- User and sign-in verification

### Use Least Privilege Access
- Security groups (App-Access-Users vs App-Access-Admins)
- Role-based access assignments
- Removing unnecessary permissions

### Assume Breach
- Sign-in monitoring
- Access reviews
- Continuous evaluation of user access

---

## Step 3 – Conditional Access Mapping

I documented how Conditional Access supports Zero Trust by:
- Requiring MFA before access is granted
- Limiting access based on user role and group membership
- Enforcing access rules even after initial sign-in

Even without active policies enabled, I demonstrated understanding of how Conditional Access reduces risk.

---

## Step 4 – Zero Trust Summary Table

| Zero Trust Principle | Identity Control Used        | Security Benefit                          |
|---------------------|-----------------------------|-------------------------------------------|
| Verify Explicitly   | MFA / Sign-in checks        | Prevents credential-based attacks         |
| Least Privilege     | Security groups & roles     | Limits access to only what’s needed       |
| Assume Breach       | Access reviews & monitoring | Reduces impact of compromised accounts    |


