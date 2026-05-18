---
name: 2-chains
description: Use when executing 2 chains protocols within the engineering sector.
---

# 2 Chains: Execution Protocol

## ⚙️ Overview
This protocol defines the exact standards for implementing 2 Chains. By following this strict operational pattern, the engine guarantees deterministic execution, high performance, and complete adherence to all architectural guardrails established by the system design.

# 2. Chains

Sequences of calls to LLMs or other utilities.

**Chain Types:**
- **LLMChain**: Basic prompt + LLM combination
- **SequentialChain**: Multiple chains in sequence
- **RouterChain**: Routes inputs to specialized chains
- **TransformChain**: Data transformations between steps
- **MapReduceChain**: Parallel processing with aggregation