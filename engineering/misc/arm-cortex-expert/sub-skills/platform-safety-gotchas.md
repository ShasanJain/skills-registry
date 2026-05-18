---
name: platform-safety-gotchas
description: Use when executing platform safety gotchas protocols within the engineering sector.
---

# Platform Safety Gotchas: Execution Protocol

## ⚙️ Overview
This protocol defines the exact standards for implementing Platform Safety Gotchas. By following this strict operational pattern, the engine guarantees deterministic execution, high performance, and complete adherence to all architectural guardrails established by the system design.

## 🛠️ Implementation SOP
Follow this step-by-step TDD procedure to execute the protocol:

- **Step 1: Baseline Context**: Verify the operational environment. Ensure required tools (like Python, Node, TS, or native CLI) are accessible before injecting new logic.
- **Step 2: Apply the Pattern**: Implement the core platform safety gotchas logic directly into the active system context.
- **Step 3: Enforce Constraints**: Check for syntax errors, injection vulnerabilities, and performance bottlenecks (`O(1)` compliance).
- **Step 4: Execute Test Suite**: Run `npm run test` or the local testing framework to ensure the logic passes all regression checks.
- **Step 5: Document and Commit**: Update the session walkthrough and sync the telemetry logs for the engineering sector.

---

## 📚 Reference Material

# Platform Safety & Gotchas

**⚠️ Voltage Tolerances:**

- Most platforms: GPIO max 3.3V (NOT 5V tolerant except STM32 FT pins)
- Use level shifters for 5V interfaces
- Check datasheet current limits (typically 6-25mA)

**Teensy 4.x:** FlexSPI dedicated to Flash/PSRAM only • EEPROM emulated (limit writes <10Hz) • LPSPI max 30MHz • Never change CCM clocks while peripherals active

**STM32 F7/H7:** Clock domain config per peripheral • Fixed DMA stream/channel assignments • GPIO speed affects slew rate/power

**nRF52:** SAADC needs calibration after power-on • GPIOTE limited (8 channels) • Radio shares priority levels

**SAMD:** SERCOM needs careful pin muxing • GCLK routing critical • Limited DMA on M0+ variants