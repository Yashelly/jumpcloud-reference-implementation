# macOS Device Enrollment – JumpCloud Agent (Workflow)

## Purpose
Document the standard workflow for enrolling a macOS device into JumpCloud using the JumpCloud Agent,
including expected scoping and validation artifacts.

This is included as part of a portfolio reference to demonstrate understanding of macOS enrollment flow
even when macOS runtime is not available in the current environment.

---

## Scope & Targeting
- **Devices:** macOS endpoints
- **Enrollment method:** JumpCloud Agent (.pkg)
- **Device Groups:** macOS workstations group (recommended)
- **Policies:** scoped via Device Groups (where applicable)
- **Network:** Not configured

Enrollment and downstream controls are intentionally scoped via **Device Groups**
to keep targeting consistent and scalable.

---

## Control Logic
High-level workflow:
1. **Admin Portal:** `Device Management` → `Devices` → `Add Device` → select **macOS**
2. Download the **JumpCloud Agent** installer (`.pkg`) or obtain the install instructions.
3. Install the agent on macOS and approve required permissions if prompted
   (e.g., under `System Settings` → `Privacy & Security`).
4. Verify the device appears in `Devices` with expected status (e.g., online / last contact).
5. Assign the device to a macOS Device Group (e.g., `DG-macOS-Workstations`).
6. Scope policies to the Device Group and validate policy application.

---

## Evidence (not captured in current environment)

---

## Design Notes
- This workflow requires a **legitimate macOS runtime on Apple hardware** (physical Mac or hosted Mac).
- No macOS enrollment artifacts are included here due to the current environment constraints.
- Windows enrollment artifacts are used as the primary hands-on evidence in this repository.

---

## Result
A documented macOS enrollment workflow is defined and ready to be executed when macOS runtime is available,
following the same scoping and validation standards used across this repository.
