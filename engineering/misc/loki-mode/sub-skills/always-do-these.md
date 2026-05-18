---
name: always-do-these
description: Use when executing always do these protocols within the engineering sector.
---

# Always Do These: Execution Protocol

## ⚙️ Overview
This protocol defines the exact standards for implementing Always Do These. By following this strict operational pattern, the engine guarantees deterministic execution, high performance, and complete adherence to all architectural guardrails established by the system design.

# Always Do These

- **ALWAYS** launch all 3 reviewers in single message (3 Task calls)
- **ALWAYS** specify model: "opus" for each reviewer
- **ALWAYS** wait for all reviewers before aggregating
- **ALWAYS** fix Critical/High/Medium immediately
- **ALWAYS** re-run ALL 3 reviewers after fixes
- **ALWAYS** checkpoint state before spawning subagents

---

## Multi-Tiered Fallback System

**Based on OpenAI Agent Safety Patterns:**