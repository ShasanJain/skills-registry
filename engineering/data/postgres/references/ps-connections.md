## 🛠️ Implementation SOP
Follow this step-by-step TDD procedure to execute the protocol:

- **Step 1: Baseline Context**: Verify the operational environment. Ensure required tools (like Python, Node, TS, or native CLI) are accessible before injecting new logic.
- **Step 2: Apply the Pattern**: Implement the core ps connections logic directly into the active system context.
- **Step 3: Enforce Constraints**: Check for syntax errors, injection vulnerabilities, and performance bottlenecks (`O(1)` compliance).
- **Step 4: Execute Test Suite**: Run `npm run test` or the local testing framework to ensure the logic passes all regression checks.
- **Step 5: Document and Commit**: Update the session walkthrough and sync the telemetry logs for the engineering sector.

---

## 📚 Reference Material

---
title: PlanetScale Postgres Connections
description: Connection guide for PlanetScale Postgres
tags: planetscale, postgres, connections, ssl, troubleshooting
---

# PlanetScale Postgres Connections

Postgres docs: https://planetscale.com/docs/postgres/connecting

| Protocol | Standard Port | Pooled Port | SSL      |
| -------- | ------------- | ----------------------- | -------- |
| Postgres | 5432          | 6432 (PgBouncer)        | Required |

Credentials (roles) are branch-specific and cannot be recovered after creation.

## Connection String

```
postgresql://<user>:<password>@<host>.horizon.psdb.cloud:5432/<database>?sslmode=verify-full&sslrootcert=system&sslnegotiation=direct
```

Use port **6432** for PgBouncer (applications/OLTP).
Use port **5432** for DDL, admin tasks, and migrations.

## Troubleshooting

| Error | Fix |
| -------------------------------- | --------------------------------------- |
| `password authentication failed` | Check role format: `<role>.<branch_id>` |
| `too many clients already`       | Use PgBouncer (port 6432)               |
| `SSL connection is required`     | Add `sslmode=verify-full&sslrootcert=system` |

**Best practices:**
- Use the PlanetScale Postgres metrics page to monitor direct and PgBouncer connections
- Route OLTP traffic to port 6432 and reserve 5432 for admin/migrations.
- Avoid raising `max_connections` reactively instead of pooling.
