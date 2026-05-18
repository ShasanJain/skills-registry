# Skill: Execution Protocol

## ⚙️ Overview
This protocol defines the exact standards for implementing Skill. By following this strict operational pattern, the engine guarantees deterministic execution, high performance, and complete adherence to all architectural guardrails established by the system design.

## 🛠️ Implementation SOP
Follow this step-by-step TDD procedure to execute the protocol:

- **Step 1: Baseline Context**: Verify the operational environment. Ensure required tools (like Python, Node, TS, or native CLI) are accessible before injecting new logic.
- **Step 2: Apply the Pattern**: Implement the core skill logic directly into the active system context.
- **Step 3: Enforce Constraints**: Check for syntax errors, injection vulnerabilities, and performance bottlenecks (`O(1)` compliance).
- **Step 4: Execute Test Suite**: Run `npm run test` or the local testing framework to ensure the logic passes all regression checks.
- **Step 5: Document and Commit**: Update the session walkthrough and sync the telemetry logs for the engineering sector.

---

## 📚 Reference Material

---
version: 4.1.0-fractal
name: firmware-analyst
description: Expert firmware analyst specializing in embedded systems, IoT
  security, and hardware reverse engineering. Masters firmware extraction,
  analysis, and vulnerability research for routers, IoT devices, automotive
  systems, and industrial controllers. Use PROACTIVELY for firmware security
  audits, IoT penetration testing, or embedded systems research.
metadata:
  model: opus
---

# Download from vendor
wget http://vendor.com/firmware/update.bin

# Extract from device via debug interface
# UART console access
screen /dev/ttyUSB0 115200
# Copy firmware partition
dd if=/dev/mtd0 of=/tmp/firmware.bin

# Extract via network protocols
# TFTP during boot
# HTTP/FTP from device web interface
```

## 🧠 Knowledge Modules (Fractal Skills)

### 1. [Hardware Methods](./sub-skills/hardware-methods.md)
### 2. [Phase 1: Identification](./sub-skills/phase-1-identification.md)
### 3. [Phase 2: Extraction](./sub-skills/phase-2-extraction.md)
### 4. [Phase 3: File System Analysis](./sub-skills/phase-3-file-system-analysis.md)
### 5. [Phase 4: Binary Analysis](./sub-skills/phase-4-binary-analysis.md)
### 6. [Authentication Issues](./sub-skills/authentication-issues.md)
### 7. [Command Injection](./sub-skills/command-injection.md)
### 8. [Memory Corruption](./sub-skills/memory-corruption.md)
### 9. [Information Disclosure](./sub-skills/information-disclosure.md)
### 10. [Extraction Tools](./sub-skills/extraction-tools.md)
### 11. [Analysis Tools](./sub-skills/analysis-tools.md)
### 12. [Emulation](./sub-skills/emulation.md)
### 13. [Hardware Tools](./sub-skills/hardware-tools.md)
### 14. [QEMU User-Mode Emulation](./sub-skills/qemu-user-mode-emulation.md)
### 15. [Full System Emulation with Firmadyne](./sub-skills/full-system-emulation-with-firmadyne.md)
### 16. [Checklist](./sub-skills/checklist.md)
### 17. [Reporting Template](./sub-skills/reporting-template.md)
### 18. [Finding 1: Title](./sub-skills/finding-1-title.md)
### 19. [Appropriate Use](./sub-skills/appropriate-use.md)
### 20. [Never Assist With](./sub-skills/never-assist-with.md)
