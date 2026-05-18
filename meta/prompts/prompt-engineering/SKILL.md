---
name: SKILL
description: Use when applying skill patterns to optimize agent workflows and prompts.
---

# Skill: Operational Execution SOP

## ⚙️ Overview
This protocol defines the strict standard for implementing Skill. By following this SOP, the engine ensures token efficiency, maximum architectural stability, and robust caching.

## 🛠️ Implementation SOP
Follow this step-by-step TDD procedure to execute the pattern:

- **Step 1: Baseline Context**: Verify the operational environment. Ensure required tools (like TS, ESLint, or native CLI) are accessible before injecting new logic.
- **Step 2: Apply the Pattern**: Implement the core skill logic into the active code or prompt block.
- **Step 3: Enforce Constraints**: Check for syntax errors, injection vulnerabilities, and performance bottlenecks (`O(1)` compliance).
- **Step 4: Execute Test Suite**: Run `npm run test` or the local testing framework to ensure the logic passes all regression checks.
- **Step 5: Document and Commit**: Update the session walkthrough and sync the telemetry logs.

---

## 📚 Reference Material

---
version: 4.1.0-fractal
name: prompt-engineering
description: Expert guide on prompt engineering patterns, best practices, and optimization techniques. Use when user wants to improve prompts, learn prompting strategies, or debug agent behavior.
---

# Prompt Engineering Patterns

Advanced prompt engineering techniques to maximize LLM performance, reliability, and controllability.

## Core Capabilities

## 🧠 Knowledge Modules (Fractal Skills)

### 1. [1. Few-Shot Learning](./sub-skills/1-few-shot-learning.md)
### 2. [2. Chain-of-Thought Prompting](./sub-skills/2-chain-of-thought-prompting.md)
### 3. [3. Prompt Optimization](./sub-skills/3-prompt-optimization.md)
### 4. [4. Template Systems](./sub-skills/4-template-systems.md)
### 5. [5. System Prompt Design](./sub-skills/5-system-prompt-design.md)
### 6. [Progressive Disclosure](./sub-skills/progressive-disclosure.md)
### 7. [Instruction Hierarchy](./sub-skills/instruction-hierarchy.md)
### 8. [Error Recovery](./sub-skills/error-recovery.md)

