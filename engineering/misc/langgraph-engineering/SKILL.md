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
name: langgraph-engineering
description: Building stateful, resilient AI agents with LangGraph v1.0.
category: orchestration
version: 4.1.0-fractal
layer: master-skill
---

# LangGraph Agent Engineering

> **Goal**: Build complex, multi-step AI workflows that are reliable, debuggable, and capable of long-running operations.

## 1. Core Concepts (The Graph)

- **State**: A explicitly defined schema (TypedDict/Pydantic) that tracks the agent's memory snapshot.
- **Nodes**: Functions that perform work (call LLM, run tool, modify state).
- **Edges**: Logic that routes flow between nodes (Conditional edges based on LLM output).

## 2. Architecture Patterns

## 🧠 Knowledge Modules (Fractal Skills)

### 1. [A. The ReAct Agent (Standard)](./sub-skills/a-the-react-agent-standard.md)
### 2. [B. Plan-and-Execute (Advanced)](./sub-skills/b-plan-and-execute-advanced.md)
### 3. [C. Human-in-the-Loop](./sub-skills/c-human-in-the-loop.md)
