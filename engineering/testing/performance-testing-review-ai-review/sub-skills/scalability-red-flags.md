---
name: scalability-red-flags
description: Use when executing scalability red flags protocols within the engineering sector.
---

# Scalability Red Flags: Execution Protocol

## ⚙️ Overview
This protocol defines the exact standards for implementing Scalability Red Flags. By following this strict operational pattern, the engine guarantees deterministic execution, high performance, and complete adherence to all architectural guardrails established by the system design.

## 🛠️ Implementation SOP
Follow this step-by-step TDD procedure to execute the protocol:

- **Step 1: Baseline Context**: Verify the operational environment. Ensure required tools (like Python, Node, TS, or native CLI) are accessible before injecting new logic.
- **Step 2: Apply the Pattern**: Implement the core scalability red flags logic directly into the active system context.
- **Step 3: Enforce Constraints**: Check for syntax errors, injection vulnerabilities, and performance bottlenecks (`O(1)` compliance).
- **Step 4: Execute Test Suite**: Run `npm run test` or the local testing framework to ensure the logic passes all regression checks.
- **Step 5: Document and Commit**: Update the session walkthrough and sync the telemetry logs for the engineering sector.

---

## 📚 Reference Material

# Scalability Red Flags

- **N+1 Queries**, **Missing Indexes**, **Synchronous External Calls**
- **In-Memory State**, **Unbounded Collections**, **Missing Pagination**
- **No Connection Pooling**, **No Rate Limiting**

```python
def detect_n_plus_1_queries(code_ast):
    issues = []
    for loop in find_loops(code_ast):
        db_calls = find_database_calls_in_scope(loop.body)
        if len(db_calls) > 0:
            issues.append({
                'severity': 'HIGH',
                'line': loop.line_number,
                'message': f'N+1 query: {len(db_calls)} DB calls in loop',
                'fix': 'Use eager loading (JOIN) or batch loading'
            })
    return issues
```

## Review Comment Generation