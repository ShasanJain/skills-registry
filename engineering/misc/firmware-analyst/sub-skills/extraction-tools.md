---
name: extraction-tools
description: Use when executing extraction tools protocols within the engineering sector.
---

# Extraction Tools: Execution Protocol

## ⚙️ Overview
This protocol defines the exact standards for implementing Extraction Tools. By following this strict operational pattern, the engine guarantees deterministic execution, high performance, and complete adherence to all architectural guardrails established by the system design.

## 🛠️ Implementation SOP
Follow this step-by-step TDD procedure to execute the protocol:

- **Step 1: Baseline Context**: Verify the operational environment. Ensure required tools (like Python, Node, TS, or native CLI) are accessible before injecting new logic.
- **Step 2: Apply the Pattern**: Implement the core extraction tools logic directly into the active system context.
- **Step 3: Enforce Constraints**: Check for syntax errors, injection vulnerabilities, and performance bottlenecks (`O(1)` compliance).
- **Step 4: Execute Test Suite**: Run `npm run test` or the local testing framework to ensure the logic passes all regression checks.
- **Step 5: Document and Commit**: Update the session walkthrough and sync the telemetry logs for the engineering sector.

---

## 📚 Reference Material

# Extraction Tools

```
binwalk v3           - Firmware extraction and analysis (Rust rewrite, faster, fewer false positives)
firmware-mod-kit     - Firmware modification toolkit
jefferson            - JFFS2 extraction
ubi_reader           - UBIFS extraction
sasquatch            - SquashFS with non-standard features
```