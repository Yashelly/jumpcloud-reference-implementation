# Windows agent enrollment

## Purpose
Enroll a Windows endpoint into JumpCloud to enable centralized device inventory,
group-based scoping, and policy enforcement via the JumpCloud agent.

---

## Scope & Targeting
- **Platform:** Windows 11
- **Enrollment type:** JumpCloud agent-based enrollment
- **Device grouping:** Assigned to `DG-Windows-Workstations` for policy scoping

---

## Implementation Summary
1. Enrolled the endpoint using the JumpCloud Windows agent.
2. Verified the device is **Active** in **Devices** and reporting telemetry.
3. Confirmed group membership is applied for scoped policy assignments.

---

## Evidence
1. **Device overview – Agent active + group scoping visible**
   `screenshots/01-device-details-agent-active-and-group-scope.png`

> Evidence is intentionally minimal and focuses on: **scope/targeting**, **control configuration**, and **validation (success)**.

---

## Result
The Windows endpoint is successfully enrolled in JumpCloud, reporting as **Active**,
and is placed into the designated device group to support group-scoped configuration and policies.
