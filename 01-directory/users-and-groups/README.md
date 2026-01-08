# Directory – Users and Groups Baseline

## Purpose
Establish a minimal user/group model for scoped enforcement (MFA/SSO) with a safe emergency access path.

---

## Scope & Targeting
- **Users:** Standard user + break-glass user (emergency access)
- **User Groups:**
  - `UG-Employees-Standard` — baseline targeting group
  - `UG-BreakGlass-Excluded` — excluded from enforcement to ensure recoverability

Users were activated immediately to enable access validation without dependency on email delivery.

---

## Evidence
1. **Standard user – Active + group membership**  
   `screenshots/01-standard_user_groups.png`

2. **Break-glass user – Active + group membership**  
   `screenshots/02-breakglass_user_groups.png`

---

## Result
Group-based targeting is established, enabling enforceable controls (MFA/SSO) while preserving emergency access.
