---
name: dos
description: Use when executing dos protocols within the engineering sector.
---

# Dos: Execution Protocol

## ⚙️ Overview
This protocol defines the exact standards for implementing Dos. By following this strict operational pattern, the engine guarantees deterministic execution, high performance, and complete adherence to all architectural guardrails established by the system design.

# Do's

- **Colocate state** - Keep state as close to where it's used as possible
- **Use selectors** - Prevent unnecessary re-renders with selective subscriptions
- **Normalize data** - Flatten nested structures for easier updates
- **Type everything** - Full TypeScript coverage prevents runtime errors
- **Separate concerns** - Server state (React Query) vs client state (Zustand)