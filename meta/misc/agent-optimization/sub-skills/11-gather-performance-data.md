---
name: 11-gather-performance-data
description: Use when applying 11 gather performance data patterns to optimize agent workflows.
---

# 11 Gather Performance Data: Standard Operating Procedure

## ⚙️ Overview
This protocol defines the strict standard for implementing 11 Gather Performance Data. By following this SOP, the engine ensures token efficiency, maximum architectural stability, robust caching, and adherence to all operational guardrails established by the system architecture.

# 1.1 Gather Performance Data

```
Use: context-manager
Command: analyze-agent-performance $ARGUMENTS --days 30
```

Collect metrics including:

- Task completion rate (successful vs failed tasks)
- Response accuracy and factual correctness
- Tool usage efficiency (correct tools, call frequency)
- Average response time and token consumption
- User satisfaction indicators (corrections, retries)
- Hallucination incidents and error patterns