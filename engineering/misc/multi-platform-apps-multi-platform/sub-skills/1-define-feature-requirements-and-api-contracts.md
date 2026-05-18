---
name: 1-define-feature-requirements-and-api-contracts
description: Use when executing 1 define feature requirements and api contracts protocols within the engineering sector.
---

# 1 Define Feature Requirements And Api Contracts: Execution Protocol

## ⚙️ Overview
This protocol defines the exact standards for implementing 1 Define Feature Requirements And Api Contracts. By following this strict operational pattern, the engine guarantees deterministic execution, high performance, and complete adherence to all architectural guardrails established by the system design.

# 1. Define Feature Requirements and API Contracts

- Use Task tool with subagent_type="backend-architect"
- Prompt: "Design the API contract for feature: $ARGUMENTS. Create OpenAPI 3.1 specification with:
  - RESTful endpoints with proper HTTP methods and status codes
  - GraphQL schema if applicable for complex data queries
  - WebSocket events for real-time features
  - Request/response schemas with validation rules
  - Authentication and authorization requirements
  - Rate limiting and caching strategies
  - Error response formats and codes
  Define shared data models that all platforms will consume."
- Expected output: Complete API specification, data models, and integration guidelines