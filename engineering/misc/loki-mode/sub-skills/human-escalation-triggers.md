---
name: human-escalation-triggers
description: Use when executing human escalation triggers protocols within the engineering sector.
---

# Human Escalation Triggers: Execution Protocol

## ⚙️ Overview
This protocol defines the exact standards for implementing Human Escalation Triggers. By following this strict operational pattern, the engine guarantees deterministic execution, high performance, and complete adherence to all architectural guardrails established by the system design.

# Human Escalation Triggers

| Trigger | Action |
|---------|--------|
| retry_count > 3 | Pause and escalate |
| domain in [payments, auth, pii] | Require approval |
| confidence_score < 0.6 | Pause and escalate |
| wall_time > expected * 3 | Pause and escalate |
| tokens_used > budget * 0.8 | Pause and escalate |

See `references/openai-patterns.md` for full fallback implementation.

---

## AGENTS.md Integration

**Read target project's AGENTS.md if exists** (OpenAI/AAIF standard):

```
Context Priority:
1. AGENTS.md (closest to current file)
2. CLAUDE.md (Claude-specific)
3. .loki/CONTINUITY.md (session state)
4. Package docs
5. README.md
```

---

## Constitutional AI Principles (Anthropic)

**Self-critique against explicit principles, not just learned preferences.**