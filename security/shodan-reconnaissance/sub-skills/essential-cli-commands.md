---
name: essential-cli-commands
description: Use when executing essential cli commands protocols within the security sector.
---

## 🛠️ Implementation SOP
Follow this step-by-step TDD procedure to execute the protocol:

- **Step 1: Baseline Context**: Verify the operational environment. Ensure required tools (like Python, Node, TS, or native CLI) are accessible before injecting new logic.
- **Step 2: Apply the Pattern**: Implement the core essential cli commands logic directly into the active system context.
- **Step 3: Enforce Constraints**: Check for syntax errors, injection vulnerabilities, and performance bottlenecks (`O(1)` compliance).
- **Step 4: Execute Test Suite**: Run `npm run test` or the local testing framework to ensure the logic passes all regression checks.
- **Step 5: Document and Commit**: Update the session walkthrough and sync the telemetry logs for the security sector.

---

## 📚 Reference Material

# Essential CLI Commands

| Command | Description | Credits |
|---------|-------------|---------|
| `shodan init KEY` | Initialize API key | 0 |
| `shodan info` | Show account info | 0 |
| `shodan myip` | Show your IP | 0 |
| `shodan host IP` | Host details | 0 |
| `shodan count QUERY` | Result count | 0 |
| `shodan search QUERY` | Basic search | 0* |
| `shodan download FILE QUERY` | Save results | 1/100 results |
| `shodan parse FILE` | Extract data | 0 |
| `shodan stats QUERY` | Statistics | 1 |
| `shodan scan submit IP` | On-demand scan | 1/IP |
| `shodan honeyscore IP` | Honeypot check | 0 |

*Filters consume 1 credit per query