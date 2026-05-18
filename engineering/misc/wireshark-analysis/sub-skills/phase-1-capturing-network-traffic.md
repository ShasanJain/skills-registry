---
name: phase-1-capturing-network-traffic
description: Use when executing phase 1 capturing network traffic protocols within the engineering sector.
---

## 🛠️ Implementation SOP
Follow this step-by-step TDD procedure to execute the protocol:

- **Step 1: Baseline Context**: Verify the operational environment. Ensure required tools (like Python, Node, TS, or native CLI) are accessible before injecting new logic.
- **Step 2: Apply the Pattern**: Implement the core phase 1 capturing network traffic logic directly into the active system context.
- **Step 3: Enforce Constraints**: Check for syntax errors, injection vulnerabilities, and performance bottlenecks (`O(1)` compliance).
- **Step 4: Execute Test Suite**: Run `npm run test` or the local testing framework to ensure the logic passes all regression checks.
- **Step 5: Document and Commit**: Update the session walkthrough and sync the telemetry logs for the engineering sector.

---

## 📚 Reference Material

# Phase 1: Capturing Network Traffic

#### Start Live Capture
Begin capturing packets on network interface:

```
1. Launch Wireshark
2. Select network interface from main screen
3. Click shark fin icon or double-click interface
4. Capture begins immediately
```

#### Capture Controls
| Action | Shortcut | Description |
|--------|----------|-------------|
| Start/Stop Capture | Ctrl+E | Toggle capture on/off |
| Restart Capture | Ctrl+R | Stop and start new capture |
| Open PCAP File | Ctrl+O | Load existing capture file |
| Save Capture | Ctrl+S | Save current capture |

#### Capture Filters
Apply filters before capture to limit data collection:

```
# Capture only specific host
host 192.168.1.100

# Capture specific port
port 80

# Capture specific network
net 192.168.1.0/24

# Exclude specific traffic
not arp

# Combine filters
host 192.168.1.100 and port 443
```