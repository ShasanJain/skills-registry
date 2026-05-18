---
name: 33-evaluation-metrics
description: Use when applying 33 evaluation metrics patterns to optimize agent workflows.
---

# 33 Evaluation Metrics: Standard Operating Procedure

## ⚙️ Overview
This protocol defines the strict standard for implementing 33 Evaluation Metrics. By following this SOP, the engine ensures token efficiency, maximum architectural stability, robust caching, and adherence to all operational guardrails established by the system architecture.

# 3.3 Evaluation Metrics

Comprehensive scoring framework:

**Task-Level Metrics:**

- Completion rate (binary success/failure)
- Correctness score (0-100% accuracy)
- Efficiency score (steps taken vs optimal)
- Tool usage appropriateness
- Response relevance and completeness

**Quality Metrics:**

- Hallucination rate (factual errors per response)
- Consistency score (alignment with previous responses)
- Format compliance (matches specified structure)
- Safety score (constraint adherence)
- User satisfaction prediction

**Performance Metrics:**

- Response latency (time to first token)
- Total generation time
- Token consumption (input + output)
- Cost per task (API usage fees)
- Memory/context efficiency