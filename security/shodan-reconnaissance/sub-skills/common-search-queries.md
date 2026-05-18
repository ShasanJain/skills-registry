---
name: common-search-queries
description: Use when executing common search queries protocols within the security sector.
---

## 🛠️ Implementation SOP
Follow this step-by-step TDD procedure to execute the protocol:

- **Step 1: Baseline Context**: Verify the operational environment. Ensure required tools (like Python, Node, TS, or native CLI) are accessible before injecting new logic.
- **Step 2: Apply the Pattern**: Implement the core common search queries logic directly into the active system context.
- **Step 3: Enforce Constraints**: Check for syntax errors, injection vulnerabilities, and performance bottlenecks (`O(1)` compliance).
- **Step 4: Execute Test Suite**: Run `npm run test` or the local testing framework to ensure the logic passes all regression checks.
- **Step 5: Document and Commit**: Update the session walkthrough and sync the telemetry logs for the security sector.

---

## 📚 Reference Material

# Common Search Queries

| Purpose | Query |
|---------|-------|
| Find webcams | `webcam has_screenshot:true` |
| MongoDB databases | `product:mongodb` |
| Redis servers | `product:redis` |
| Elasticsearch | `product:elastic port:9200` |
| Default passwords | `"default password"` |
| Vulnerable RDP | `port:3389 vuln:CVE-2019-0708` |
| Industrial systems | `port:502 modbus` |
| Cisco devices | `product:cisco` |
| Open VNC | `port:5900 authentication disabled` |
| Exposed FTP | `port:21 anonymous` |
| WordPress sites | `http.component:wordpress` |
| Printers | `"HP-ChaiSOE" port:80` |
| Cameras (RTSP) | `port:554 has_screenshot:true` |
| Jenkins servers | `X-Jenkins port:8080` |
| Docker APIs | `port:2375 product:docker` |