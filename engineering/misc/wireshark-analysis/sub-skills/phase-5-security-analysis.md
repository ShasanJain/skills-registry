---
name: phase-5-security-analysis
description: Use when executing phase 5 security analysis protocols within the engineering sector.
---

# Phase 5 Security Analysis: Execution Protocol

## ⚙️ Overview
This protocol defines the exact standards for implementing Phase 5 Security Analysis. By following this strict operational pattern, the engine guarantees deterministic execution, high performance, and complete adherence to all architectural guardrails established by the system design.

## 🛠️ Implementation SOP
Follow this step-by-step TDD procedure to execute the protocol:

- **Step 1: Baseline Context**: Verify the operational environment. Ensure required tools (like Python, Node, TS, or native CLI) are accessible before injecting new logic.
- **Step 2: Apply the Pattern**: Implement the core phase 5 security analysis logic directly into the active system context.
- **Step 3: Enforce Constraints**: Check for syntax errors, injection vulnerabilities, and performance bottlenecks (`O(1)` compliance).
- **Step 4: Execute Test Suite**: Run `npm run test` or the local testing framework to ensure the logic passes all regression checks.
- **Step 5: Document and Commit**: Update the session walkthrough and sync the telemetry logs for the engineering sector.

---

## 📚 Reference Material

# Phase 5: Security Analysis

#### Detect Port Scanning
Identify reconnaissance activity:

```
# SYN scan detection (many ports, same source)
ip.src == SUSPECT_IP && tcp.flags.syn == 1

# Review Statistics > Conversations for anomalies
# Look for single source hitting many destination ports
```

#### Identify Suspicious Traffic
Filter for anomalies:

```
# Traffic to unusual ports
tcp.dstport > 1024 && tcp.dstport < 49152

# Traffic outside trusted network
!(ip.addr == 192.168.1.0/24)

# Unusual DNS queries
dns.qry.name contains "suspicious-domain"

# Large data transfers
frame.len > 1400
```

#### ARP Spoofing Detection
Identify ARP attacks:

```
# Duplicate ARP responses
arp.duplicate-address-frame

# ARP traffic analysis
arp

# Look for:
# - Multiple MACs for same IP
# - Gratuitous ARP floods
# - Unusual ARP patterns
```

#### Examine Downloads
Analyze file transfers:

```
# HTTP file downloads
http.request.method == "GET" && http contains "Content-Disposition"

# Follow HTTP Stream to view file content
# Use File > Export Objects > HTTP to extract files
```

#### DNS Analysis
Investigate DNS activity:

```
# All DNS traffic
dns

# DNS queries only
dns.flags.response == 0

# DNS responses only
dns.flags.response == 1

# Failed DNS lookups
dns.flags.rcode != 0

# Specific domain queries
dns.qry.name contains "domain.com"
```