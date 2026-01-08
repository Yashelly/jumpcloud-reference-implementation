# Password Policies – Employees Baseline and Break-glass

## Purpose
Establish strong, group-scoped password requirements for standard users while maintaining a reliable emergency access path.

---

## Scope & Targeting
- **Employees baseline:** `UG-Employees-Standard`
  - **Policy:** `PP-Employees-Standard`
- **Break-glass:** `UG-BreakGlass-Excluded`
  - **Policy:** `PP-BreakGlass`

Password requirements are intentionally scoped via **User Groups** to keep enforcement consistent and maintainable.

---

## Control Logic

### PP-Employees-Standard (UG-Employees-Standard)
- **Minimum length:** 14 characters
- **Complexity:** lowercase, uppercase, number, special character
- **Password bans:** common passwords, username inclusion, repeated/sequential characters
- **Aging:** history (5), expiration (90 days)
- **Lockout:** 8 failed attempts, auto-unlock (10 minutes), counter reset (30 minutes)

### PP-BreakGlass (UG-BreakGlass-Excluded)
- **Minimum length:** 20 characters
- **Complexity:** lowercase, uppercase, number, special character
- **Password bans:** common passwords, username inclusion, repeated/sequential characters
- **Aging:** history (10)
- **Expiration:** intentionally not enforced to preserve emergency access reliability
- **Lockout:** 10 failed attempts, auto-unlock (10 minutes), counter reset (30 minutes)

Self-service password reset without MFA enrollment is not enabled.

---

## Evidence
1. **Employees policy – assignment and settings**  
   `screenshots/1-policy-assignment-and-settings.png`

2. **Break-glass policy – assignment and settings**  
   `screenshots/02-breakglass-policy-assignment-and-settings.png`

---

## Result
Group-scoped password controls enforce a strong baseline for standard users while preserving a separate break-glass path designed for recoverability.
