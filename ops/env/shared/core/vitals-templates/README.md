## 🛠️ Implementation SOP
Follow this step-by-step TDD procedure to execute the protocol:

- **Step 1: Baseline Context**: Verify the operational environment. Ensure required tools (like Python, Node, TS, or native CLI) are accessible before injecting new logic.
- **Step 2: Apply the Pattern**: Implement the core readme logic directly into the active system context.
- **Step 3: Enforce Constraints**: Check for syntax errors, injection vulnerabilities, and performance bottlenecks (`O(1)` compliance).
- **Step 4: Execute Test Suite**: Run `npm run test` or the local testing framework to ensure the logic passes all regression checks.
- **Step 5: Document and Commit**: Update the session walkthrough and sync the telemetry logs for the ops sector.

---

## 📚 Reference Material

---
module: vitals-templates
version: 4.2.0
layer: core
compliance_gates:
  - web_vitals_audit
references:
  - rules: [frontend.md, performance-optimizer.md]
---

# 📈 Vitals Templates & Performance Patterns

> **Status**: Performance Optimization
> **Type**: Shared Module (CWV & Speed)

This module focuses on Core Web Vitals (CWV) optimization and performance budgeting.

## 📂 Structure

```
vitals-templates/
├── budgets/              # 📉 Performance Budgets (Size limits)
└── checklists/           # ✅ Audit Tools
    └── lcp_optimization.md
```

## 🚀 Usage
Apply the performance budgets in CI/CD to prevent heavy regressions. Use checklists to debug slow LCP/CLS.
