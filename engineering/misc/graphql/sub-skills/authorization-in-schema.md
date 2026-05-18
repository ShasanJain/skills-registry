---
name: authorization-in-schema
description: Use when executing authorization in schema protocols within the engineering sector.
---

## 🛠️ Implementation SOP
Follow this step-by-step TDD procedure to execute the protocol:

- **Step 1: Baseline Context**: Verify the operational environment. Ensure required tools (like Python, Node, TS, or native CLI) are accessible before injecting new logic.
- **Step 2: Apply the Pattern**: Implement the core authorization in schema logic directly into the active system context.
- **Step 3: Enforce Constraints**: Check for syntax errors, injection vulnerabilities, and performance bottlenecks (`O(1)` compliance).
- **Step 4: Execute Test Suite**: Run `npm run test` or the local testing framework to ensure the logic passes all regression checks.
- **Step 5: Document and Commit**: Update the session walkthrough and sync the telemetry logs for the engineering sector.

---

## 📚 Reference Material

# ❌ Authorization in Schema

## ⚠️ Sharp Edges

| Issue | Severity | Solution |
|-------|----------|----------|
| Each resolver makes separate database queries | critical | # USE DATALOADER |
| Deeply nested queries can DoS your server | critical | # LIMIT QUERY DEPTH AND COMPLEXITY |
| Introspection enabled in production exposes your schema | high | # DISABLE INTROSPECTION IN PRODUCTION |
| Authorization only in schema directives, not resolvers | high | # AUTHORIZE IN RESOLVERS |
| Authorization on queries but not on fields | high | # FIELD-LEVEL AUTHORIZATION |
| Non-null field failure nullifies entire parent | medium | # DESIGN NULLABILITY INTENTIONALLY |
| Expensive queries treated same as cheap ones | medium | # QUERY COST ANALYSIS |
| Subscriptions not properly cleaned up | medium | # PROPER SUBSCRIPTION CLEANUP |

## Related Skills

Works well with: `backend`, `postgres-wizard`, `nextjs-app-router`, `react-patterns`