---
name: 51-file-system-bunfile
description: Use when executing 51 file system bunfile protocols within the engineering sector.
---

# 51 File System Bunfile: Execution Protocol

## ⚙️ Overview
This protocol defines the exact standards for implementing 51 File System Bunfile. By following this strict operational pattern, the engine guarantees deterministic execution, high performance, and complete adherence to all architectural guardrails established by the system design.

## 🛠️ Implementation SOP
Follow this step-by-step TDD procedure to execute the protocol:

- **Step 1: Baseline Context**: Verify the operational environment. Ensure required tools (like Python, Node, TS, or native CLI) are accessible before injecting new logic.
- **Step 2: Apply the Pattern**: Implement the core 51 file system bunfile logic directly into the active system context.
- **Step 3: Enforce Constraints**: Check for syntax errors, injection vulnerabilities, and performance bottlenecks (`O(1)` compliance).
- **Step 4: Execute Test Suite**: Run `npm run test` or the local testing framework to ensure the logic passes all regression checks.
- **Step 5: Document and Commit**: Update the session walkthrough and sync the telemetry logs for the engineering sector.

---

## 📚 Reference Material

# 5.1 File System (Bun.file)

```typescript
// Read file
const file = Bun.file("./data.json");
const text = await file.text();
const json = await file.json();
const buffer = await file.arrayBuffer();

// File info
console.log(file.size); // bytes
console.log(file.type); // MIME type

// Write file
await Bun.write("./output.txt", "Hello, Bun!");
await Bun.write("./data.json", JSON.stringify({ foo: "bar" }));

// Stream large files
const reader = file.stream();
for await (const chunk of reader) {
  console.log(chunk);
}
```