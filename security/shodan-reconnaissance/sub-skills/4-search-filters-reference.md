---
name: 4-search-filters-reference
description: Use when executing 4 search filters reference protocols within the security sector.
---

# 4 Search Filters Reference: Execution Protocol

## ⚙️ Overview
This protocol defines the exact standards for implementing 4 Search Filters Reference. By following this strict operational pattern, the engine guarantees deterministic execution, high performance, and complete adherence to all architectural guardrails established by the system design.

## 🛠️ Implementation SOP
Follow this step-by-step TDD procedure to execute the protocol:

- **Step 1: Baseline Context**: Verify the operational environment. Ensure required tools (like Python, Node, TS, or native CLI) are accessible before injecting new logic.
- **Step 2: Apply the Pattern**: Implement the core 4 search filters reference logic directly into the active system context.
- **Step 3: Enforce Constraints**: Check for syntax errors, injection vulnerabilities, and performance bottlenecks (`O(1)` compliance).
- **Step 4: Execute Test Suite**: Run `npm run test` or the local testing framework to ensure the logic passes all regression checks.
- **Step 5: Document and Commit**: Update the session walkthrough and sync the telemetry logs for the security sector.

---

## 📚 Reference Material

# 4. Search Filters Reference

#### Network Filters
```
ip:1.2.3.4                  # Specific IP address
net:192.168.0.0/24          # Network range (CIDR)
hostname:example.com        # Hostname contains
port:22                     # Specific port
asn:AS15169                 # Autonomous System Number
```

#### Geographic Filters
```
country:US                  # Two-letter country code
country:"United States"     # Full country name
city:"San Francisco"        # City name
state:CA                    # State/region
postal:94102                # Postal/ZIP code
geo:37.7,-122.4             # Lat/long coordinates
```

#### Organization Filters
```
org:"Google"                # Organization name
isp:"Comcast"               # ISP name
```

#### Service/Product Filters
```
product:nginx               # Software product
version:1.14.0              # Software version
os:"Windows Server 2019"    # Operating system
http.title:"Dashboard"      # HTTP page title
http.html:"login"           # HTML content
http.status:200             # HTTP status code
ssl.cert.subject.cn:*.example.com  # SSL certificate
ssl:true                    # Has SSL enabled
```

#### Vulnerability Filters
```
vuln:CVE-2019-0708          # Specific CVE
has_vuln:true               # Has any vulnerability
```

#### Screenshot Filters
```
has_screenshot:true         # Has screenshot available
screenshot.label:webcam     # Screenshot type
```