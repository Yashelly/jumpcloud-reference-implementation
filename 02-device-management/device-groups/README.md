# Device groups

## Purpose
Create a predictable device grouping model for scope-based policy assignment, reporting, and future platform expansion (Windows/macOS).

---

## Scope & Targeting
- **Platforms:** Windows, macOS (future), plus built-in platform groups (Linux/iOS/Android)
- **Group types:**
  - **Dynamic (built-in):** automatically populated platform groups (e.g., *Windows Devices*, *Mac Devices*, *All Devices*)
  - **Static (custom):** manually controlled scope groups for enterprise-style assignments
- **Naming standard (custom):**
  - `DG-<Platform>-<DeviceClass>` (e.g., `DG-Windows-Workstations`, `DG-Mac-Workstations`)
- **Why static groups for workstations:**
  - predictable scoping for policies and commands
  - mirrors typical enterprise operational model (explicit target groups)
- **Exclusion model (custom):**
  - `DG-Excluded-From-Policies` — explicit “exclude bucket” for devices that must not receive baseline policies (lab/test/breakglass devices)

---

## Implementation Summary
1. Reviewed the built-in **Dynamic** device groups created by JumpCloud.
2. Created custom **Static** device groups:
   - `DG-Windows-Workstations`
   - `DG-Mac-Workstations` *(prepared for future macOS enrollment and policy scoping)*
   - `DG-Excluded-From-Policies` *(centralized exclusion target for safe testing / exception handling)*
3. Verified in **Device Management** → **Device Groups** list that:
   - groups are present
   - **Device Membership Controls** reflect the intended type (**Static** for `DG-*`, **Dynamic** for built-ins)

---

## Evidence
1. **Device groups list (baseline + custom groups visible, including membership type)**
   - `screenshots/01-device-groups-overview.png`

> Evidence is intentionally minimal and focuses on: **scope/targeting**, **control configuration**, and **validation (success)**.

---

## Result
A clean device-group baseline is in place: built-in **Dynamic** platform groups for automatic inventory + custom **Static** workstation and exclusion groups for predictable, enterprise-style scoping and safe exception management.
