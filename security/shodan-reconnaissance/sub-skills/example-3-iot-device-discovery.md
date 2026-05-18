---
name: example-3-iot-device-discovery
description: Use when executing example 3 iot device discovery protocols within the security sector.
---

# Example 3 Iot Device Discovery: Execution Protocol

## ⚙️ Overview
This protocol defines the exact standards for implementing Example 3 Iot Device Discovery. By following this strict operational pattern, the engine guarantees deterministic execution, high performance, and complete adherence to all architectural guardrails established by the system design.

## 🛠️ Implementation SOP
Follow this step-by-step TDD procedure to execute the protocol:

- **Step 1: Baseline Context**: Verify the operational environment. Ensure required tools (like Python, Node, TS, or native CLI) are accessible before injecting new logic.
- **Step 2: Apply the Pattern**: Implement the core example 3 iot device discovery logic directly into the active system context.
- **Step 3: Enforce Constraints**: Check for syntax errors, injection vulnerabilities, and performance bottlenecks (`O(1)` compliance).
- **Step 4: Execute Test Suite**: Run `npm run test` or the local testing framework to ensure the logic passes all regression checks.
- **Step 5: Document and Commit**: Update the session walkthrough and sync the telemetry logs for the security sector.

---

## 📚 Reference Material

# Example 3: IoT Device Discovery

```bash
# Find exposed webcams
shodan search 'webcam has_screenshot:true country:US'

# Find industrial control systems
shodan search 'port:502 product:modbus'

# Find exposed printers
shodan search '"HP-ChaiSOE" port:80'

# Find smart home devices
shodan search 'product:nest'
```