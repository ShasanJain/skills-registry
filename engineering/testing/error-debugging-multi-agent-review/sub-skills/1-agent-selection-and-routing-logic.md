---
name: 1-agent-selection-and-routing-logic
description: Use when executing 1 agent selection and routing logic protocols within the engineering sector.
---

# 1 Agent Selection And Routing Logic: Execution Protocol

## ⚙️ Overview
This protocol defines the exact standards for implementing 1 Agent Selection And Routing Logic. By following this strict operational pattern, the engine guarantees deterministic execution, high performance, and complete adherence to all architectural guardrails established by the system design.

# 1. Agent Selection and Routing Logic

- **Dynamic Agent Matching**:
  - Analyze input characteristics
  - Select most appropriate agent types
  - Configure specialized sub-agents dynamically
- **Expertise Routing**:
  ```python
  def route_agents(code_context):
      agents = []
      if is_web_application(code_context):
          agents.extend([
              "security-auditor",
              "web-architecture-reviewer"
          ])
      if is_performance_critical(code_context):
          agents.append("performance-analyst")
      return agents
  ```