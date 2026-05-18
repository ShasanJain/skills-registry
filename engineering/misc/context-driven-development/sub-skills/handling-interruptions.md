---
name: handling-interruptions
description: Use when executing handling interruptions protocols within the engineering sector.
---

# Handling Interruptions: Execution Protocol

## ⚙️ Overview
This protocol defines the exact standards for implementing Handling Interruptions. By following this strict operational pattern, the engine guarantees deterministic execution, high performance, and complete adherence to all architectural guardrails established by the system design.

# Handling Interruptions

If interrupted mid-task:

1. Mark task as `[~]` with note about stopping point
2. Commit work-in-progress to feature branch
3. Document any uncommitted decisions in plan.md

## Best Practices

1. **Read context first**: Always read relevant artifacts before starting work
2. **Small updates**: Make incremental context changes, not massive rewrites
3. **Link decisions**: Reference context when making implementation choices
4. **Version context**: Commit context changes alongside code changes
5. **Review context**: Include context artifact reviews in code reviews
6. **Validate regularly**: Run context validation checklist before major work
7. **Communicate changes**: Notify team when context artifacts change significantly
8. **Preserve history**: Use git to track context evolution over time
9. **Question staleness**: If context feels wrong, investigate and update
10. **Keep it actionable**: Every context item should inform a decision or behavior