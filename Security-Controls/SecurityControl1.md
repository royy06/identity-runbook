# Security Controls

## Purpose
This document outlines the security controls implemented across the identity environment used for all projects in this repository.

---

## Multi-Factor Authentication (MFA)
- MFA is enforced for all user accounts.
- Security Defaults are enabled to require MFA during sign-in.
- MFA strengthens authentication by requiring additional verification beyond username and password.

---

## Least Privilege Access
- Access is granted through security group membership only.
- Users are assigned to groups based on role (e.g., HR, IT).
- No direct permissions are assigned to individual user accounts.

---

## Account Protection
- Strong password requirements are enforced.
- Account lockout occurs after multiple failed login attempts.
- Password reset procedures are documented and followed.

---

## Identity Governance
- User access follows Joiner, Mover, and Leaver (JML) principles.
- Access reviews are supported through group membership validation.

---

## Monitoring and Review
- User sign-in activity is monitored through Entra ID.
- Group memberships are reviewed periodically to ensure continued access is appropriate.

---

## Notes
These security controls apply across all projects unless otherwise specified.

