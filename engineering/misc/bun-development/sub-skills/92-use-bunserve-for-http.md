---
name: 92-use-bunserve-for-http
description: Use when executing 92 use bunserve for http protocols within the engineering sector.
---

# 92 Use Bunserve For Http: Execution Protocol

## ⚙️ Overview
This protocol defines the exact standards for implementing 92 Use Bunserve For Http. By following this strict operational pattern, the engine guarantees deterministic execution, high performance, and complete adherence to all architectural guardrails established by the system design.

## 🛠️ Implementation SOP
Follow this step-by-step TDD procedure to execute the protocol:

- **Step 1: Baseline Context**: Verify the operational environment. Ensure required tools (like Python, Node, TS, or native CLI) are accessible before injecting new logic.
- **Step 2: Apply the Pattern**: Implement the core 92 use bunserve for http logic directly into the active system context.
- **Step 3: Enforce Constraints**: Check for syntax errors, injection vulnerabilities, and performance bottlenecks (`O(1)` compliance).
- **Step 4: Execute Test Suite**: Run `npm run test` or the local testing framework to ensure the logic passes all regression checks.
- **Step 5: Document and Commit**: Update the session walkthrough and sync the telemetry logs for the engineering sector.

---

## 📚 Reference Material

# 9.2 Use Bun.serve for HTTP

```typescript
// Don't: Express/Fastify (overhead)
import express from "express";
const app = express();

// Do: Bun.serve (native, 4-10x faster)
Bun.serve({
  fetch(req) {
    return new Response("Hello!");
  },
});

// Or use Elysia (Bun-optimized framework)
import { Elysia } from "elysia";
new Elysia().get("/", () => "Hello!").listen(3000);
```