---
name: multi-tool-static-analysis
description: Use when executing multi tool static analysis protocols within the engineering sector.
---

# Multi Tool Static Analysis: Execution Protocol

## ⚙️ Overview
This protocol defines the exact standards for implementing Multi Tool Static Analysis. By following this strict operational pattern, the engine guarantees deterministic execution, high performance, and complete adherence to all architectural guardrails established by the system design.

# Multi-Tool Static Analysis

Execute in parallel:
- **CodeQL**: Deep vulnerability analysis (SQL injection, XSS, auth bypasses)
- **SonarQube**: Code smells, complexity, duplication, maintainability
- **Semgrep**: Organization-specific rules and security policies
- **Snyk/Dependabot**: Supply chain security
- **GitGuardian/TruffleHog**: Secret detection