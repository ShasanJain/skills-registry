---
name: example-6-network-range-assessment
description: Use when executing example 6 network range assessment protocols within the security sector.
---

## 🛠️ Implementation SOP
Follow this step-by-step TDD procedure to execute the protocol:

- **Step 1: Baseline Context**: Verify the operational environment. Ensure required tools (like Python, Node, TS, or native CLI) are accessible before injecting new logic.
- **Step 2: Apply the Pattern**: Implement the core example 6 network range assessment logic directly into the active system context.
- **Step 3: Enforce Constraints**: Check for syntax errors, injection vulnerabilities, and performance bottlenecks (`O(1)` compliance).
- **Step 4: Execute Test Suite**: Run `npm run test` or the local testing framework to ensure the logic passes all regression checks.
- **Step 5: Document and Commit**: Update the session walkthrough and sync the telemetry logs for the security sector.

---

## 📚 Reference Material

# Example 6: Network Range Assessment

```bash
# Scan a /24 network range
shodan search 'net:192.168.1.0/24'

# Get port distribution
shodan stats --facets port 'net:192.168.1.0/24'

# Find specific vulnerabilities in range
shodan search 'net:192.168.1.0/24 vuln:CVE-2021-44228'

# Export all data for range
shodan download network_scan.json.gz 'net:192.168.1.0/24'
```

## Troubleshooting

| Issue | Cause | Solution |
|-------|-------|----------|
| No API Key Configured | Key not initialized | Run `shodan init YOUR_API_KEY` then verify with `shodan info` |
| Query Credits Exhausted | Monthly credits consumed | Use credit-free queries (no filters), wait for reset, or upgrade |
| Host Recently Crawled | Cannot re-scan IP within 24h | Use `shodan host IP` for existing data, or wait 24 hours |
| Rate Limit Exceeded | >1 request/second | Add `time.sleep(1)` between API requests |
| Empty Search Results | Too specific or syntax error | Use quotes for phrases: `'org:"Company Name"'`; broaden criteria |
| Downloaded File Won't Parse | Corrupted or wrong format | Verify with `gunzip -t file.gz`, re-download with `--limit` |