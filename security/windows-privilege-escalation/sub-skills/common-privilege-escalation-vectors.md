---
name: common-privilege-escalation-vectors
description: Use when executing common privilege escalation vectors protocols within the security sector.
---

## 🛠️ Implementation SOP
Follow this step-by-step TDD procedure to execute the protocol:

- **Step 1: Baseline Context**: Verify the operational environment. Ensure required tools (like Python, Node, TS, or native CLI) are accessible before injecting new logic.
- **Step 2: Apply the Pattern**: Implement the core common privilege escalation vectors logic directly into the active system context.
- **Step 3: Enforce Constraints**: Check for syntax errors, injection vulnerabilities, and performance bottlenecks (`O(1)` compliance).
- **Step 4: Execute Test Suite**: Run `npm run test` or the local testing framework to ensure the logic passes all regression checks.
- **Step 5: Document and Commit**: Update the session walkthrough and sync the telemetry logs for the security sector.

---

## 📚 Reference Material

# Common Privilege Escalation Vectors

| Vector | Check Command |
|--------|---------------|
| Unquoted paths | `wmic service get pathname \| findstr /i /v """` |
| Weak service perms | `accesschk.exe -uwcqv "Everyone" *` |
| AlwaysInstallElevated | `reg query HKCU\...\Installer /v AlwaysInstallElevated` |
| Stored credentials | `cmdkey /list` |
| Token privileges | `whoami /priv` |
| Scheduled tasks | `schtasks /query /fo LIST /v` |