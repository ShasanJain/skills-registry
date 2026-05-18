## 🛠️ Implementation SOP
Follow this step-by-step TDD procedure to execute the protocol:

- **Step 1: Baseline Context**: Verify the operational environment. Ensure required tools (like Python, Node, TS, or native CLI) are accessible before injecting new logic.
- **Step 2: Apply the Pattern**: Implement the core ps extensions logic directly into the active system context.
- **Step 3: Enforce Constraints**: Check for syntax errors, injection vulnerabilities, and performance bottlenecks (`O(1)` compliance).
- **Step 4: Execute Test Suite**: Run `npm run test` or the local testing framework to ensure the logic passes all regression checks.
- **Step 5: Document and Commit**: Update the session walkthrough and sync the telemetry logs for the engineering sector.

---

## 📚 Reference Material

---
title: PlanetScale PostgreSQL Extensions
description: Extension reference
tags: postgres, extensions
---

# PostgreSQL Extensions on PlanetScale

Only use PlanetScale-supported extensions. For the complete and up-to-date list of available extensions, see: https://planetscale.com/docs/postgres/extensions

Do not rely on hard-coded extension lists — always check the documentation above for current availability.

## Enabling Extensions

Some extensions must first be **enabled in the PlanetScale Dashboard** (Clusters > Extensions) before they can be created in SQL. This often requires a database restart.

Once enabled in the dashboard, create the extension in SQL:

```sql
CREATE EXTENSION IF NOT EXISTS <extension_name>;
```

## Recommended Patterns

- Always check the [PlanetScale extensions docs](https://planetscale.com/docs/postgres/extensions) before assuming an extension is available.
- Verify extension availability in PlanetScale configuration and docs before schema design depends on it.
- Enable `pg_stat_statements` early for baseline query telemetry.
