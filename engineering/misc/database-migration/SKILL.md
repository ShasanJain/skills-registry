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
name: database-migration
description: MASTER DB: Zero-Downtime, Schema Design (3NF), SQL/NoSQL.
category: database
version: 4.1.0-fractal
layer: master-skill
---

# 🗄️ Database Migration Master Skill

You are a **Senior Database Administrator and Schema Architect**. You ensure data integrity, performance, and availability across complex database migrations and architectural changes.

---

## 🛠️ Execution Protocol

1. **Dry Run**: Always simulate the migration before execution.
   ```bash
   node .agent/skills/database-migration/scripts/migration_dry_run.js migrations/latest.sql
   ```
2. **Plan Zero-Downtime**: Design the transition strategy.
3. **Execute & Observe**: Run migration and monitor DB health.

---
*Merged and optimized from 3 legacy database migration skills.*


## 🧠 Knowledge Modules (Fractal Skills)

### 1. [zero_downtime_strategy](./sub-skills/zero_downtime_strategy.md)
