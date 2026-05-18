---
name: operational-security
description: Use when executing operational security protocols within the security sector.
---

## 🛠️ Implementation SOP
Follow this step-by-step TDD procedure to execute the protocol:

- **Step 1: Baseline Context**: Verify the operational environment. Ensure required tools (like Python, Node, TS, or native CLI) are accessible before injecting new logic.
- **Step 2: Apply the Pattern**: Implement the core operational security logic directly into the active system context.
- **Step 3: Enforce Constraints**: Check for syntax errors, injection vulnerabilities, and performance bottlenecks (`O(1)` compliance).
- **Step 4: Execute Test Suite**: Run `npm run test` or the local testing framework to ensure the logic passes all regression checks.
- **Step 5: Document and Commit**: Update the session walkthrough and sync the telemetry logs for the security sector.

---

## 📚 Reference Material

# Operational Security

- Use encrypted channels (reverse_https) when possible
- Clean up artifacts after testing
- Avoid detection by monitoring systems
- Limit post-exploitation to agreed scope

## Troubleshooting

| Issue | Solutions |
|-------|-----------|
| Database not connected | Run `sudo msfdb init`, start PostgreSQL, then `db_connect` |
| Exploit fails/no session | Run `check`; verify payload architecture; check firewall; try different payloads |
| Session dies immediately | Migrate to stable process; use stageless payload; check AV; use AutoRunScript |
| Payload detected by AV | Use encoding `-e x86/shikata_ga_nai -i 10`; use evasion modules; custom templates |