---
name: phase-4-binary-analysis
description: Use when executing phase 4 binary analysis protocols within the engineering sector.
---

# Phase 4 Binary Analysis: Execution Protocol

## ⚙️ Overview
This protocol defines the exact standards for implementing Phase 4 Binary Analysis. By following this strict operational pattern, the engine guarantees deterministic execution, high performance, and complete adherence to all architectural guardrails established by the system design.

## 🛠️ Implementation SOP
Follow this step-by-step TDD procedure to execute the protocol:

- **Step 1: Baseline Context**: Verify the operational environment. Ensure required tools (like Python, Node, TS, or native CLI) are accessible before injecting new logic.
- **Step 2: Apply the Pattern**: Implement the core phase 4 binary analysis logic directly into the active system context.
- **Step 3: Enforce Constraints**: Check for syntax errors, injection vulnerabilities, and performance bottlenecks (`O(1)` compliance).
- **Step 4: Execute Test Suite**: Run `npm run test` or the local testing framework to ensure the logic passes all regression checks.
- **Step 5: Document and Commit**: Update the session walkthrough and sync the telemetry logs for the engineering sector.

---

## 📚 Reference Material

# Phase 4: Binary Analysis

```bash
# Identify architecture
file bin/httpd
readelf -h bin/httpd

# Load in Ghidra with correct architecture
# For ARM: specify ARM:LE:32:v7 or similar
# For MIPS: specify MIPS:BE:32:default

# Set up cross-compilation for testing
# ARM
arm-linux-gnueabi-gcc exploit.c -o exploit
# MIPS
mipsel-linux-gnu-gcc exploit.c -o exploit
```

## Common Vulnerability Classes