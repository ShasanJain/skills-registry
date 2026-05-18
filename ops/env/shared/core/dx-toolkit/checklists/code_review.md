---
name: code_review
description: Use when executing code_review protocols within the ops sector.
---

# Code_Review: Execution Protocol

## ⚙️ Overview
This protocol defines the exact standards for implementing Code_Review. By following this strict operational pattern, the engine guarantees deterministic execution, high performance, and complete adherence to all architectural guardrails established by the system design.

# ✅ Code Review Checklist

> check_type: manual_audit
> priority: medium

## 1. Logic & Correctness
- [ ] **Edge Cases**: Are null/undefined values handled?
- [ ] **Complexity**: Is there any nested loop (O(n^2)) that can be optimized?
- [ ] **Dead Code**: Are there unused variables or imports?

## 2. Readability (Clean Code)
- [ ] **Naming**: Do variables explain *what* they contain (e.g. `userList` vs `data`)?
- [ ] **Functions**: Are functions small (< 20 lines) and do one thing?
- [ ] **Comments**: Do comments explain *WHY*, not *WHAT*?

## 3. Testing
- [ ] **Coverage**: Is there a test case for this new feature?
- [ ] **Regression**: Does this break existing tests?
