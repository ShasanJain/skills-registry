# Skill: Execution Protocol

## ⚙️ Overview
This protocol defines the exact standards for implementing Skill. By following this strict operational pattern, the engine guarantees deterministic execution, high performance, and complete adherence to all architectural guardrails established by the system design.

## 🛠️ Implementation SOP
Follow this step-by-step TDD procedure to execute the protocol:

- **Step 1: Baseline Context**: Verify the operational environment. Ensure required tools (like Python, Node, TS, or native CLI) are accessible before injecting new logic.
- **Step 2: Apply the Pattern**: Implement the core skill logic directly into the active system context.
- **Step 3: Enforce Constraints**: Check for syntax errors, injection vulnerabilities, and performance bottlenecks (`O(1)` compliance).
- **Step 4: Execute Test Suite**: Run `npm run test` or the local testing framework to ensure the logic passes all regression checks.
- **Step 5: Document and Commit**: Update the session walkthrough and sync the telemetry logs for the engineering sector.

---

## 📚 Reference Material

---
name: performance-profiling
description: Performance profiling principles. Measurement, analysis, and optimization techniques.
category: infrastructure
version: 4.1.0-fractal
layer: master-skill
---

# Performance Profiling

> Measure, analyze, optimize - in that order.

## 🔧 Runtime Scripts

**Execute these for automated profiling:**

| Script | Purpose | Usage |
|--------|---------|-------|
| `scripts/lighthouse_audit.py` | Lighthouse performance audit | `python scripts/lighthouse_audit.py https://example.com` |

---

## 1. Core Web Vitals

## 🧠 Knowledge Modules (Fractal Skills)

### 1. [Targets](./sub-skills/targets.md)
### 2. [When to Measure](./sub-skills/when-to-measure.md)
### 3. [The 4-Step Process](./sub-skills/the-4-step-process.md)
### 4. [Profiling Tool Selection](./sub-skills/profiling-tool-selection.md)
### 5. [What to Look For](./sub-skills/what-to-look-for.md)
### 6. [Optimization Actions](./sub-skills/optimization-actions.md)
### 7. [Performance Tab Analysis](./sub-skills/performance-tab-analysis.md)
### 8. [Memory Tab Analysis](./sub-skills/memory-tab-analysis.md)
### 9. [By Symptom](./sub-skills/by-symptom.md)
