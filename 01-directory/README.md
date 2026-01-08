# Directory – Users, Groups, and Password Policy Baseline

## Purpose
Establish a minimal JumpCloud directory model (users + groups) and apply group-scoped password controls to support consistent enforcement and safe recoverability.

---

## Scope & Targeting
- **Users:** standard user + break-glass user (emergency access)
- **User Groups:**
  - `UG-Employees-Standard` — baseline targeting group for standard users
  - `UG-BreakGlass-Excluded` — emergency access group kept separate from baseline enforcement

Users were activated immediately to enable access validation without dependency on email delivery.

---

## Implemented Controls
### Users and Groups
- Standard user is bound to `UG-Employees-Standard`
- Break-glass user is bound to `UG-BreakGlass-Excluded`
- Group model is used for scoping of downstream controls (MFA/SSO) and operational separation

### Password Policies (group-scoped)
- **PP-Employees-Standard** → `UG-Employees-Standard`
  - 14-character minimum, complexity requirements, history/expiration, and lockout protections
- **PP-BreakGlass** → `UG-BreakGlass-Excluded`
  - 20-character minimum, stricter history and lockout
  - password expiration intentionally not enforced to preserve emergency access reliability

---

## Evidence Standard
Evidence is intentionally minimal and focuses on:
- **scope/targeting**
- **control configuration**
- **validation readiness**

All screenshots/artifacts are sanitized to remove PII and secrets.

---

## Contents
- `users-and-groups/` — directory objects and scoping groups
- `password-policy/` — group-scoped password policies and assignments

---

## Result
A group-based directory baseline is established with enforceable password controls for standard users and a separate break-glass path designed for recoverability.
