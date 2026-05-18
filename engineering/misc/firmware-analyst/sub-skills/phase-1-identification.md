---
name: phase-1-identification
description: Use when executing phase 1 identification protocols within the engineering sector.
---

# Phase 1 Identification: Execution Protocol

## ⚙️ Overview
This protocol defines the exact standards for implementing Phase 1 Identification. By following this strict operational pattern, the engine guarantees deterministic execution, high performance, and complete adherence to all architectural guardrails established by the system design.

## 🛠️ Implementation SOP
Follow this step-by-step TDD procedure to execute the protocol:

- **Step 1: Baseline Context**: Verify the operational environment. Ensure required tools (like Python, Node, TS, or native CLI) are accessible before injecting new logic.
- **Step 2: Apply the Pattern**: Implement the core phase 1 identification logic directly into the active system context.
- **Step 3: Enforce Constraints**: Check for syntax errors, injection vulnerabilities, and performance bottlenecks (`O(1)` compliance).
- **Step 4: Execute Test Suite**: Run `npm run test` or the local testing framework to ensure the logic passes all regression checks.
- **Step 5: Document and Commit**: Update the session walkthrough and sync the telemetry logs for the engineering sector.

---

## 📚 Reference Material

# Phase 1: Identification

```bash
# Basic file identification
file firmware.bin
binwalk firmware.bin

# Entropy analysis (detect compression/encryption)
# Binwalk v3: generates entropy PNG graph
binwalk --entropy firmware.bin
binwalk -E firmware.bin  # Short form

# Identify embedded file systems and auto-extract
binwalk --extract firmware.bin
binwalk -e firmware.bin  # Short form

# String analysis
strings -a firmware.bin | grep -i "password\|key\|secret"
```