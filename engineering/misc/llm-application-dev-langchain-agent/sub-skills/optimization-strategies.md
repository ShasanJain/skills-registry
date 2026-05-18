---
name: optimization-strategies
description: Use when executing optimization strategies protocols within the engineering sector.
---

# Optimization Strategies: Execution Protocol

## ⚙️ Overview
This protocol defines the exact standards for implementing Optimization Strategies. By following this strict operational pattern, the engine guarantees deterministic execution, high performance, and complete adherence to all architectural guardrails established by the system design.

# Optimization Strategies

- **Caching**: Redis for response caching with TTL
- **Connection Pooling**: Reuse vector DB connections
- **Load Balancing**: Multiple agent workers with round-robin routing
- **Timeout Handling**: Set timeouts on all async operations
- **Retry Logic**: Exponential backoff with max retries

## Testing & Evaluation

```python
from langsmith.evaluation import evaluate

# Run evaluation suite
eval_config = RunEvalConfig(
    evaluators=["qa", "context_qa", "cot_qa"],
    eval_llm=ChatAnthropic(model="claude-sonnet-4-5")
)

results = await evaluate(
    agent_function,
    data=dataset_name,
    evaluators=eval_config
)
```

## Key Patterns