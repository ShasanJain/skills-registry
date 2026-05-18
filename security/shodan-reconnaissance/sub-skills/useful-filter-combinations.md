---
name: useful-filter-combinations
description: Use when executing useful filter combinations protocols within the security sector.
---

## 🛠️ Implementation SOP
Follow this step-by-step TDD procedure to execute the protocol:

- **Step 1: Baseline Context**: Verify the operational environment. Ensure required tools (like Python, Node, TS, or native CLI) are accessible before injecting new logic.
- **Step 2: Apply the Pattern**: Implement the core useful filter combinations logic directly into the active system context.
- **Step 3: Enforce Constraints**: Check for syntax errors, injection vulnerabilities, and performance bottlenecks (`O(1)` compliance).
- **Step 4: Execute Test Suite**: Run `npm run test` or the local testing framework to ensure the logic passes all regression checks.
- **Step 5: Document and Commit**: Update the session walkthrough and sync the telemetry logs for the security sector.

---

## 📚 Reference Material

# Useful Filter Combinations

| Scenario | Query |
|---------|-------|
| Target org recon | `org:"Company Name"` |
| Domain enumeration | `hostname:example.com` |
| Network range scan | `net:192.168.0.0/24` |
| SSL cert search | `ssl.cert.subject.cn:*.target.com` |
| Vulnerable servers | `vuln:CVE-2021-44228 country:US` |
| Exposed admin panels | `http.title:"admin" port:443` |
| Database exposure | `port:3306,5432,27017,6379` |