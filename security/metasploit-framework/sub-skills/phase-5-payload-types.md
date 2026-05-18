---
name: phase-5-payload-types
description: Use when executing phase 5 payload types protocols within the security sector.
---

# Phase 5 Payload Types: Execution Protocol

## ⚙️ Overview
This protocol defines the exact standards for implementing Phase 5 Payload Types. By following this strict operational pattern, the engine guarantees deterministic execution, high performance, and complete adherence to all architectural guardrails established by the system design.

## 🛠️ Implementation SOP
Follow this step-by-step TDD procedure to execute the protocol:

- **Step 1: Baseline Context**: Verify the operational environment. Ensure required tools (like Python, Node, TS, or native CLI) are accessible before injecting new logic.
- **Step 2: Apply the Pattern**: Implement the core phase 5 payload types logic directly into the active system context.
- **Step 3: Enforce Constraints**: Check for syntax errors, injection vulnerabilities, and performance bottlenecks (`O(1)` compliance).
- **Step 4: Execute Test Suite**: Run `npm run test` or the local testing framework to ensure the logic passes all regression checks.
- **Step 5: Document and Commit**: Update the session walkthrough and sync the telemetry logs for the security sector.

---

## 📚 Reference Material

# Phase 5: Payload Types

Select appropriate payload for the situation:

```bash
# Singles - Self-contained, no staging
windows/shell_reverse_tcp
linux/x86/shell_bind_tcp

# Stagers - Small payload that downloads larger stage
windows/meterpreter/reverse_tcp
linux/x86/meterpreter/bind_tcp

# Stages - Downloaded by stager, provides full functionality
# Meterpreter, VNC, shell

# Payload naming convention:
# [platform]/[architecture]/[payload_type]/[connection_type]
# Examples:
windows/x64/meterpreter/reverse_tcp
linux/x86/shell/bind_tcp
php/meterpreter/reverse_tcp
java/meterpreter/reverse_https
android/meterpreter/reverse_tcp
```