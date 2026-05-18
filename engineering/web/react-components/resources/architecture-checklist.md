---
name: architecture-checklist
description: Use when executing architecture checklist protocols within the engineering sector.
---

# Architecture Checklist: Execution Protocol

## ⚙️ Overview
This protocol defines the exact standards for implementing Architecture Checklist. By following this strict operational pattern, the engine guarantees deterministic execution, high performance, and complete adherence to all architectural guardrails established by the system design.

# Architecture Quality Gate

### Structural integrity
- [ ] Logic extracted to custom hooks in `src/hooks/`.
- [ ] No monolithic files; strictly Atomic/Composite modularity.
- [ ] All static text/URLs moved to `src/data/mockData.ts`.

### Type safety and syntax
- [ ] Props use `Readonly<T>` interfaces.
- [ ] File is syntactically valid TypeScript (no red squiggles).
- [ ] Placeholders from templates (e.g., `StitchComponent`) have been replaced with actual names.

### Styling and theming
- [ ] Dark mode (`dark:`) applied to all color classes.
- [ ] No hardcoded hex values; use theme-mapped Tailwind classes.