---
name: essential-msfconsole-commands
description: Use when executing essential msfconsole commands protocols within the security sector.
---

## 🛠️ Implementation SOP
Follow this step-by-step TDD procedure to execute the protocol:

- **Step 1: Baseline Context**: Verify the operational environment. Ensure required tools (like Python, Node, TS, or native CLI) are accessible before injecting new logic.
- **Step 2: Apply the Pattern**: Implement the core essential msfconsole commands logic directly into the active system context.
- **Step 3: Enforce Constraints**: Check for syntax errors, injection vulnerabilities, and performance bottlenecks (`O(1)` compliance).
- **Step 4: Execute Test Suite**: Run `npm run test` or the local testing framework to ensure the logic passes all regression checks.
- **Step 5: Document and Commit**: Update the session walkthrough and sync the telemetry logs for the security sector.

---

## 📚 Reference Material

# Essential MSFConsole Commands

| Command | Description |
|---------|-------------|
| `search [term]` | Search for modules |
| `use [module]` | Select a module |
| `info` | Display module information |
| `show options` | Show configurable options |
| `set [OPT] [val]` | Set option value |
| `setg [OPT] [val]` | Set global option |
| `run` / `exploit` | Execute module |
| `check` | Verify target vulnerability |
| `back` | Deselect module |
| `sessions -l` | List active sessions |
| `sessions -i [N]` | Interact with session |
| `jobs -l` | List background jobs |
| `db_nmap` | Run nmap with database |