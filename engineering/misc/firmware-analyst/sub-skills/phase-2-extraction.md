---
name: phase-2-extraction
description: Use when executing phase 2 extraction protocols within the engineering sector.
---

# Phase 2 Extraction: Execution Protocol

## ⚙️ Overview
This protocol defines the exact standards for implementing Phase 2 Extraction. By following this strict operational pattern, the engine guarantees deterministic execution, high performance, and complete adherence to all architectural guardrails established by the system design.

## 🛠️ Implementation SOP
Follow this step-by-step TDD procedure to execute the protocol:

- **Step 1: Baseline Context**: Verify the operational environment. Ensure required tools (like Python, Node, TS, or native CLI) are accessible before injecting new logic.
- **Step 2: Apply the Pattern**: Implement the core phase 2 extraction logic directly into the active system context.
- **Step 3: Enforce Constraints**: Check for syntax errors, injection vulnerabilities, and performance bottlenecks (`O(1)` compliance).
- **Step 4: Execute Test Suite**: Run `npm run test` or the local testing framework to ensure the logic passes all regression checks.
- **Step 5: Document and Commit**: Update the session walkthrough and sync the telemetry logs for the engineering sector.

---

## 📚 Reference Material

# Phase 2: Extraction

```bash
# Binwalk v3 recursive extraction (matryoshka mode)
binwalk --extract --matryoshka firmware.bin
binwalk -eM firmware.bin  # Short form

# Extract to custom directory
binwalk -e -C ./extracted firmware.bin

# Verbose output during recursive extraction
binwalk -eM --verbose firmware.bin

# Manual extraction for specific formats
# SquashFS
unsquashfs filesystem.squashfs

# JFFS2
jefferson filesystem.jffs2 -d output/

# UBIFS
ubireader_extract_images firmware.ubi

# YAFFS
unyaffs filesystem.yaffs

# Cramfs
cramfsck -x output/ filesystem.cramfs
```