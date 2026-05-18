---
name: 2-context-management-and-state-passing
description: Use when executing 2 context management and state passing protocols within the engineering sector.
---

# 2 Context Management And State Passing: Execution Protocol

## ⚙️ Overview
This protocol defines the exact standards for implementing 2 Context Management And State Passing. By following this strict operational pattern, the engine guarantees deterministic execution, high performance, and complete adherence to all architectural guardrails established by the system design.

# 2. Context Management and State Passing

- **Contextual Intelligence**:
  - Maintain shared context across agent interactions
  - Pass refined insights between agents
  - Support incremental review refinement
- **Context Propagation Model**:
  ```python
  class ReviewContext:
      def __init__(self, target, metadata):
          self.target = target
          self.metadata = metadata
          self.agent_insights = {}

      def update_insights(self, agent_type, insights):
          self.agent_insights[agent_type] = insights
  ```