---
name: 43-environment-variables
description: Use when executing 43 environment variables protocols within the engineering sector.
---

# 43 Environment Variables: Execution Protocol

## ⚙️ Overview
This protocol defines the exact standards for implementing 43 Environment Variables. By following this strict operational pattern, the engine guarantees deterministic execution, high performance, and complete adherence to all architectural guardrails established by the system design.

## 🛠️ Implementation SOP
Follow this step-by-step TDD procedure to execute the protocol:

- **Step 1: Baseline Context**: Verify the operational environment. Ensure required tools (like Python, Node, TS, or native CLI) are accessible before injecting new logic.
- **Step 2: Apply the Pattern**: Implement the core 43 environment variables logic directly into the active system context.
- **Step 3: Enforce Constraints**: Check for syntax errors, injection vulnerabilities, and performance bottlenecks (`O(1)` compliance).
- **Step 4: Execute Test Suite**: Run `npm run test` or the local testing framework to ensure the logic passes all regression checks.
- **Step 5: Document and Commit**: Update the session walkthrough and sync the telemetry logs for the engineering sector.

---

## 📚 Reference Material

# 4.3 Environment Variables

```typescript
// .env file is loaded automatically!

// Access environment variables
const apiKey = Bun.env.API_KEY;
const port = Bun.env.PORT ?? "3000";

// Or use process.env (Node.js compatible)
const dbUrl = process.env.DATABASE_URL;
```

```bash
# Run with specific env file
bun --env-file=.env.production run index.ts
```

---

## 5. Built-in APIs