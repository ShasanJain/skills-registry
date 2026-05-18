---
name: example-2-vulnerable-service-discovery
description: Use when executing example 2 vulnerable service discovery protocols within the security sector.
---

# Example 2 Vulnerable Service Discovery: Execution Protocol

## ⚙️ Overview
This protocol defines the exact standards for implementing Example 2 Vulnerable Service Discovery. By following this strict operational pattern, the engine guarantees deterministic execution, high performance, and complete adherence to all architectural guardrails established by the system design.

## 🛠️ Implementation SOP
Follow this step-by-step TDD procedure to execute the protocol:

- **Step 1: Baseline Context**: Verify the operational environment. Ensure required tools (like Python, Node, TS, or native CLI) are accessible before injecting new logic.
- **Step 2: Apply the Pattern**: Implement the core example 2 vulnerable service discovery logic directly into the active system context.
- **Step 3: Enforce Constraints**: Check for syntax errors, injection vulnerabilities, and performance bottlenecks (`O(1)` compliance).
- **Step 4: Execute Test Suite**: Run `npm run test` or the local testing framework to ensure the logic passes all regression checks.
- **Step 5: Document and Commit**: Update the session walkthrough and sync the telemetry logs for the security sector.

---

## 📚 Reference Material

# Example 2: Vulnerable Service Discovery

```bash
# Find hosts vulnerable to BlueKeep (RDP CVE)
shodan search 'vuln:CVE-2019-0708 country:US'

# Find exposed Elasticsearch with no auth
shodan search 'product:elastic port:9200 -authentication'

# Find Log4j vulnerable systems
shodan search 'vuln:CVE-2021-44228'
```