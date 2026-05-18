---
name: 6-statistics-and-analysis
description: Use when executing 6 statistics and analysis protocols within the security sector.
---

# 6 Statistics And Analysis: Execution Protocol

## ⚙️ Overview
This protocol defines the exact standards for implementing 6 Statistics And Analysis. By following this strict operational pattern, the engine guarantees deterministic execution, high performance, and complete adherence to all architectural guardrails established by the system design.

## 🛠️ Implementation SOP
Follow this step-by-step TDD procedure to execute the protocol:

- **Step 1: Baseline Context**: Verify the operational environment. Ensure required tools (like Python, Node, TS, or native CLI) are accessible before injecting new logic.
- **Step 2: Apply the Pattern**: Implement the core 6 statistics and analysis logic directly into the active system context.
- **Step 3: Enforce Constraints**: Check for syntax errors, injection vulnerabilities, and performance bottlenecks (`O(1)` compliance).
- **Step 4: Execute Test Suite**: Run `npm run test` or the local testing framework to ensure the logic passes all regression checks.
- **Step 5: Document and Commit**: Update the session walkthrough and sync the telemetry logs for the security sector.

---

## 📚 Reference Material

# 6. Statistics and Analysis

#### Get Search Statistics
```bash
# Default statistics (top 10 countries, orgs)
shodan stats nginx

# Custom facets
shodan stats --facets domain,port,asn --limit 5 nginx

# Save to CSV
shodan stats --facets country,org -O stats.csv apache
```