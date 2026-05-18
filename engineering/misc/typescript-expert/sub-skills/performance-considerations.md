---
name: performance-considerations
description: Use when executing performance considerations protocols within the engineering sector.
---

# Performance Considerations: Execution Protocol

## ⚙️ Overview
This protocol defines the exact standards for implementing Performance Considerations. By following this strict operational pattern, the engine guarantees deterministic execution, high performance, and complete adherence to all architectural guardrails established by the system design.

# Performance Considerations

- [ ] Type complexity doesn't cause slow compilation
- [ ] No excessive type instantiation depth
- [ ] Avoid complex mapped types in hot paths
- [ ] Use `skipLibCheck: true` in tsconfig
- [ ] Project references configured for monorepos