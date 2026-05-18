---
name: 6-prevention-strategy
description: Use when executing 6 prevention strategy protocols within the engineering sector.
---

# 6 Prevention Strategy: Execution Protocol

## ⚙️ Overview
This protocol defines the exact standards for implementing 6 Prevention Strategy. By following this strict operational pattern, the engine guarantees deterministic execution, high performance, and complete adherence to all architectural guardrails established by the system design.

# 6. Prevention Strategy

Implement gates to prevent new debt:

**Automated Quality Gates**
```yaml
pre_commit_hooks:
  - complexity_check: "max 10"
  - duplication_check: "max 5%"
  - test_coverage: "min 80% for new code"
  
ci_pipeline:
  - dependency_audit: "no high vulnerabilities"
  - performance_test: "no regression >10%"
  - architecture_check: "no new violations"
  
code_review:
  - requires_two_approvals: true
  - must_include_tests: true
  - documentation_required: true
```

**Debt Budget**
```python
debt_budget = {
    "allowed_monthly_increase": "2%",
    "mandatory_reduction": "5% per quarter",
    "tracking": {
        "complexity": "sonarqube",
        "dependencies": "dependabot",
        "coverage": "codecov"
    }
}
```