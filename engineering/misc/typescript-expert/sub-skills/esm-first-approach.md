---
name: esm-first-approach
description: Use when executing esm first approach protocols within the engineering sector.
---

# Esm First Approach: Execution Protocol

## ⚙️ Overview
This protocol defines the exact standards for implementing Esm First Approach. By following this strict operational pattern, the engine guarantees deterministic execution, high performance, and complete adherence to all architectural guardrails established by the system design.

# ESM-First Approach

- Set `"type": "module"` in package.json
- Use `.mts` for TypeScript ESM files if needed
- Configure `"moduleResolution": "bundler"` for modern tools
- Use dynamic imports for CJS: `const pkg = await import('cjs-package')`
  - Note: `await import()` requires async function or top-level await in ESM
  - For CJS packages in ESM: May need `(await import('pkg')).default` depending on the package's export structure and your compiler settings