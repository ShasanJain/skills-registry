---
name: with-rag-systems
description: Use when applying with rag systems patterns to optimize agent workflows and prompts.
---

# With Rag Systems: Operational Execution SOP

## ⚙️ Overview
This protocol defines the strict standard for implementing With Rag Systems. By following this SOP, the engine ensures token efficiency, maximum architectural stability, and robust caching.

## 🛠️ Implementation SOP
Follow this step-by-step TDD procedure to execute the pattern:

- **Step 1: Baseline Context**: Verify the operational environment. Ensure required tools (like TS, ESLint, or native CLI) are accessible before injecting new logic.
- **Step 2: Apply the Pattern**: Implement the core with rag systems logic into the active code or prompt block.
- **Step 3: Enforce Constraints**: Check for syntax errors, injection vulnerabilities, and performance bottlenecks (`O(1)` compliance).
- **Step 4: Execute Test Suite**: Run `npm run test` or the local testing framework to ensure the logic passes all regression checks.
- **Step 5: Document and Commit**: Update the session walkthrough and sync the telemetry logs.

---

## 📚 Reference Material

# With RAG Systems

```python
# Combine retrieved context with prompt engineering
prompt = f"""Given the following context:
{retrieved_context}

{few_shot_examples}

Question: {user_question}

Provide a detailed answer based solely on the context above. If the context doesn't contain enough information, explicitly state what's missing."""
```
