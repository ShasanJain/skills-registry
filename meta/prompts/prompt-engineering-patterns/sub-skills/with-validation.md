---
name: with-validation
description: Use when applying with validation patterns to optimize agent workflows and prompts.
---

# With Validation: Operational Execution SOP

## ⚙️ Overview
This protocol defines the strict standard for implementing With Validation. By following this SOP, the engine ensures token efficiency, maximum architectural stability, and robust caching.

## 🛠️ Implementation SOP
Follow this step-by-step TDD procedure to execute the pattern:

- **Step 1: Baseline Context**: Verify the operational environment. Ensure required tools (like TS, ESLint, or native CLI) are accessible before injecting new logic.
- **Step 2: Apply the Pattern**: Implement the core with validation logic into the active code or prompt block.
- **Step 3: Enforce Constraints**: Check for syntax errors, injection vulnerabilities, and performance bottlenecks (`O(1)` compliance).
- **Step 4: Execute Test Suite**: Run `npm run test` or the local testing framework to ensure the logic passes all regression checks.
- **Step 5: Document and Commit**: Update the session walkthrough and sync the telemetry logs.

---

## 📚 Reference Material

# With Validation

```python
# Add self-verification step
prompt = f"""{main_task_prompt}

After generating your response, verify it meets these criteria:
1. Answers the question directly
2. Uses only information from provided context
3. Cites specific sources
4. Acknowledges any uncertainty

If verification fails, revise your response."""
```

## Performance Optimization
