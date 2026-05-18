---
name: 41-version-management
description: Use when applying 41 version management patterns to optimize agent workflows.
---

# 41 Version Management: Standard Operating Procedure

## ⚙️ Overview
This protocol defines the strict standard for implementing 41 Version Management. By following this SOP, the engine ensures token efficiency, maximum architectural stability, robust caching, and adherence to all operational guardrails established by the system architecture.

## 🛠️ Implementation SOP
Follow this step-by-step TDD procedure to execute the pattern:

- **Step 1: Baseline Context**: Verify the operational environment. Ensure required tools (like TS, ESLint, or native CLI) are accessible before injecting new logic.
- **Step 2: Apply the Pattern**: Implement the core 41 version management logic into the active code or prompt block.
- **Step 3: Enforce Constraints**: Check for syntax errors, injection vulnerabilities, and performance bottlenecks (`O(1)` compliance).
- **Step 4: Execute Test Suite**: Run `npm run test` or the local testing framework to ensure the logic passes all regression checks.
- **Step 5: Document and Commit**: Update the session walkthrough and sync the telemetry logs.

---

## 📚 Reference Material

# 4.1 Version Management

Systematic versioning strategy:

```
Version Format: agent-name-v[MAJOR].[MINOR].[PATCH]
Example: customer-support-v2.3.1

MAJOR: Significant capability changes
MINOR: Prompt improvements, new examples
PATCH: Bug fixes, minor adjustments
```

Maintain version history:

- Git-based prompt storage
- Changelog with improvement details
- Performance metrics per version
- Rollback procedures documented