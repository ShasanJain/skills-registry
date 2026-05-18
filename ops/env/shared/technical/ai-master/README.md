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
module: ai-master
version: 4.2.0
layer: technical
compliance_gates:
  - prompt_audit
  - agency_verification
references:
  - rules: [ai-engineer.md, langgraph-engineering.md]
---

# 🤖 AI Master & Agentic Design Patterns

> **Status**: Core Capability
> **Type**: Shared Module (Prompts & Patterns)

This module provides the intelligence backbone for AI Agent operations, including standardized prompt patterns and model configurations.

## 📂 Structure

```
ai-master/
├── best_patterns.md      # 📜 Theory & Strategy (Existing)
├── checklists/           # ✅ Audit Tools
│   └── prompt_audit.md   #    - Verify prompt quality & safety
└── presets/              # ⚙️ Configuration
    └── model_configs.json #    - Recommended params for Gemini/GPT
```

## 🚀 Usage

### 1. Model Selection
Use `presets/model_configs.json` to configure the optimal temperature and tokens for your task (Creative vs. Biological vs. Coding).

### 2. Prompt Engineering
Before sending a heavy prompt, audit it against `checklists/prompt_audit.md` to ensure it follows the "Chain of Thought" or "ReAct" standards.
