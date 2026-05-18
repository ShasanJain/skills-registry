---
name: 22-few-shot-example-optimization
description: Use when applying 22 few shot example optimization patterns to optimize agent workflows.
---

# 22 Few Shot Example Optimization: Standard Operating Procedure

## ⚙️ Overview
This protocol defines the strict standard for implementing 22 Few Shot Example Optimization. By following this SOP, the engine ensures token efficiency, maximum architectural stability, robust caching, and adherence to all operational guardrails established by the system architecture.

# 2.2 Few-Shot Example Optimization

Curate high-quality examples from successful interactions:

- **Select diverse examples** covering common use cases
- **Include edge cases** that previously failed
- **Show both positive and negative examples** with explanations
- **Order examples** from simple to complex
- **Annotate examples** with key decision points

Example structure:

```
Good Example:
Input: [User request]
Reasoning: [Step-by-step thought process]
Output: [Successful response]
Why this works: [Key success factors]

Bad Example:
Input: [Similar request]
Output: [Failed response]
Why this fails: [Specific issues]
Correct approach: [Fixed version]
```