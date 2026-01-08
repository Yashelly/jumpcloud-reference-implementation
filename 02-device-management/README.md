# Device management

## Purpose
Implement a device management baseline in JumpCloud covering endpoint enrollment, device grouping, and
validation artifacts for Windows and macOS (workflow-only where runtime is unavailable).

This section focuses on **agent-based enrollment**, **group-based scoping**, and **evidence-driven validation**
to mirror an enterprise device lifecycle model.

---

## Scope & Targeting
- **Platforms:**
  - **Windows:** implemented (hands-on)
  - **macOS:** workflow documented (no macOS runtime in this environment)
- **Enrollment method:** JumpCloud Agent
  - Windows: MSI / PowerShell installer
  - macOS: PKG installer (workflow)
- **Scoping model:** **Device Groups** (recommended)
  - Built-in platform groups (Dynamic) remain as baseline inventory
  - Custom scope groups (Static) used for predictable targeting (e.g., workstations)
- **Policies:** out of scope in this folder (covered under `03-policies/`)
- **Network:** not configured

---

## Repository structure
- `device-groups/` — device grouping model (Dynamic vs Static) used for scalable targeting
- `windows-agent-enrollment/` — Windows enrollment via JumpCloud Agent + validation evidence
- `macos-agent-enrollment/` — macOS enrollment workflow (documented, not executed)

---

## Implementation Summary
1. Established the **device group baseline** and created custom scope groups for workstations.
2. Enrolled a **Windows 11** endpoint using the JumpCloud Agent.
3. Verified device visibility in **Devices**, agent status, and group membership for scoping.
4. Documented the macOS enrollment workflow to demonstrate understanding of cross-platform operations
   despite environment constraints.

---

## Evidence
### Windows (captured)
- Windows agent enrollment validation:
  - `windows-agent-enrollment/screenshots/01-device-details-agent-active-and-group-scope.png`

### Device groups (captured)
- Device group baseline + custom groups:
  - `device-groups/screenshots/01-device-groups-overview.png`
  - `device-groups/screenshots/02-device-groups-custom-workstations.png`

### macOS (not captured)
- No artifacts included (see `macos-agent-enrollment/README.md` for rationale)

> Evidence is intentionally minimal and focuses on: **scope/targeting**, **control configuration**, and **validation (success)**.

---

## Result
A practical device management baseline is established:
- **Windows** endpoint is successfully enrolled via the JumpCloud Agent and scoped through device groups.
- **macOS** enrollment flow is documented and ready for execution when a macOS runtime is available.
