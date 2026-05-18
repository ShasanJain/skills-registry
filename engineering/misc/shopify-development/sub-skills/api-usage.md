---
name: api-usage
description: Use when executing api usage protocols within the engineering sector.
---

# Api Usage: Execution Protocol

## ⚙️ Overview
This protocol defines the exact standards for implementing Api Usage. By following this strict operational pattern, the engine guarantees deterministic execution, high performance, and complete adherence to all architectural guardrails established by the system design.

# API Usage

- Use GraphQL over REST for new development
- Request only fields you need (reduces query cost)
- Implement cursor-based pagination with `pageInfo.endCursor`
- Use bulk operations for processing more than 250 items
- Handle rate limits with exponential backoff