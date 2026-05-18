---
name: 3-parallel-vs-sequential-execution
description: Use when executing 3 parallel vs sequential execution protocols within the engineering sector.
---

# 3 Parallel Vs Sequential Execution: Execution Protocol

## ⚙️ Overview
This protocol defines the exact standards for implementing 3 Parallel Vs Sequential Execution. By following this strict operational pattern, the engine guarantees deterministic execution, high performance, and complete adherence to all architectural guardrails established by the system design.

# 3. Parallel vs Sequential Execution

- **Hybrid Execution Strategy**:
  - Parallel execution for independent reviews
  - Sequential processing for dependent insights
  - Intelligent timeout and fallback mechanisms
- **Execution Flow**:
  ```python
  def execute_review(review_context):
      # Parallel independent agents
      parallel_agents = [
          "code-quality-reviewer",
          "security-auditor"
      ]

      # Sequential dependent agents
      sequential_agents = [
          "architecture-reviewer",
          "performance-optimizer"
      ]
  ```