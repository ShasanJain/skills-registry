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
name: filesystem-mcp
description: Official Filesystem Model Context Protocol Server for local file operations.
category: tools
version: 4.1.0-fractal
layer: master-skill
---

# Filesystem MCP Skill

## 🎯 Goal
Enable the AI Agent to read, write, and manage files on the local filesystem securely using the official Model Context Protocol standard.

## 🛠️ Tools

## 🧠 Knowledge Modules (Fractal Skills)

### 1. [`read_file`](./sub-skills/read_file.md)
### 2. [`write_file`](./sub-skills/write_file.md)
### 3. [`list_directory`](./sub-skills/list_directory.md)
### 4. [`move_file`](./sub-skills/move_file.md)
### 5. [`search_files`](./sub-skills/search_files.md)
