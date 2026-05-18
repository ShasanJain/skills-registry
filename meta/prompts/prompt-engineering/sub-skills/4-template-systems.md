---
name: 4-template-systems
description: Use when applying 4 template systems patterns to optimize agent workflows and prompts.
---

# 4 Template Systems: Operational Execution SOP

## ⚙️ Overview
This protocol defines the strict standard for implementing 4 Template Systems. By following this SOP, the engine ensures token efficiency, maximum architectural stability, and robust caching.

## 🛠️ Implementation SOP
Follow this step-by-step TDD procedure to execute the pattern:

- **Step 1: Baseline Context**: Verify the operational environment. Ensure required tools (like TS, ESLint, or native CLI) are accessible before injecting new logic.
- **Step 2: Apply the Pattern**: Implement the core 4 template systems logic into the active code or prompt block.
- **Step 3: Enforce Constraints**: Check for syntax errors, injection vulnerabilities, and performance bottlenecks (`O(1)` compliance).
- **Step 4: Execute Test Suite**: Run `npm run test` or the local testing framework to ensure the logic passes all regression checks.
- **Step 5: Document and Commit**: Update the session walkthrough and sync the telemetry logs.

---

## 📚 Reference Material

# 4. Template Systems

Build reusable prompt structures with variables, conditional sections, and modular components. Use for multi-turn conversations, role-based interactions, or when the same pattern applies to different inputs. Reduces duplication and ensures consistency across similar tasks.

**Example:**

```python
# Reusable code review template
template = """
Review this {language} code for {focus_area}.

Code:
{code_block}

Provide feedback on:
{checklist}
"""

# Usage
prompt = template.format(
    language="Python",
    focus_area="security vulnerabilities",
    code_block=user_code,
    checklist="1. SQL injection\n2. XSS risks\n3. Authentication"
)
```
