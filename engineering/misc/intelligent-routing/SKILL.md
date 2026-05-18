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
name: intelligent-routing
description: Automatic agent selection and intelligent task routing.
category: tools
version: 4.1.0-fractal
layer: master-skill
---

# Intelligent Agent Routing

**Purpose**: Automatically analyze user requests and route them to the most appropriate specialist agent(s) without requiring explicit user mentions.

## Core Principle

> **The AI should act as an intelligent Project Manager**, analyzing each request and automatically selecting the best specialist(s) for the job.

## How It Works

## 🧠 Knowledge Modules (Fractal Skills)

### 1. [1. Request Analysis](./sub-skills/1-request-analysis.md)
### 2. [2. Agent Selection Matrix](./sub-skills/2-agent-selection-matrix.md)
### 3. [3. Automatic Routing Protocol](./sub-skills/3-automatic-routing-protocol.md)
### 4. [Single-Domain Tasks (Auto-invoke Single Agent)](./sub-skills/single-domain-tasks-auto-invoke-single-agent.md)
### 5. [Multi-Domain Tasks (Auto-invoke Orchestrator)](./sub-skills/multi-domain-tasks-auto-invoke-orchestrator.md)
### 6. [SIMPLE (Direct agent invocation)](./sub-skills/simple-direct-agent-invocation.md)
### 7. [MODERATE (2-3 agents)](./sub-skills/moderate-2-3-agents.md)
### 8. [COMPLEX (Orchestrator required)](./sub-skills/complex-orchestrator-required.md)
### 9. [Rule 1: Silent Analysis](./sub-skills/rule-1-silent-analysis.md)
### 10. [Rule 2: Inform Agent Selection](./sub-skills/rule-2-inform-agent-selection.md)
### 11. [Rule 3: Seamless Experience](./sub-skills/rule-3-seamless-experience.md)
### 12. [Rule 4: Override Capability](./sub-skills/rule-4-override-capability.md)
### 13. [Case 1: Generic Question](./sub-skills/case-1-generic-question.md)
### 14. [Case 2: Extremely Vague Request](./sub-skills/case-2-extremely-vague-request.md)
### 15. [Case 3: Contradictory Patterns](./sub-skills/case-3-contradictory-patterns.md)
### 16. [With /orchestrate Command](./sub-skills/with-orchestrate-command.md)
### 17. [With Socratic Gate](./sub-skills/with-socratic-gate.md)
### 18. [With GEMINI.md Rules](./sub-skills/with-geminimd-rules.md)
### 19. [Test Cases](./sub-skills/test-cases.md)
### 20. [Token Usage](./sub-skills/token-usage.md)
### 21. [Response Time](./sub-skills/response-time.md)
### 22. [Optional: First-Time Explanation](./sub-skills/optional-first-time-explanation.md)
### 23. [Enable Debug Mode (for development)](./sub-skills/enable-debug-mode-for-development.md)
