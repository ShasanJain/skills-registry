---
name: 23-edit-tool-design
description: Use when executing 23 edit tool design protocols within the engineering sector.
---

# 23 Edit Tool Design: Execution Protocol

## ⚙️ Overview
This protocol defines the exact standards for implementing 23 Edit Tool Design. By following this strict operational pattern, the engine guarantees deterministic execution, high performance, and complete adherence to all architectural guardrails established by the system design.

## 🛠️ Implementation SOP
Follow this step-by-step TDD procedure to execute the protocol:

- **Step 1: Baseline Context**: Verify the operational environment. Ensure required tools (like Python, Node, TS, or native CLI) are accessible before injecting new logic.
- **Step 2: Apply the Pattern**: Implement the core 23 edit tool design logic directly into the active system context.
- **Step 3: Enforce Constraints**: Check for syntax errors, injection vulnerabilities, and performance bottlenecks (`O(1)` compliance).
- **Step 4: Execute Test Suite**: Run `npm run test` or the local testing framework to ensure the logic passes all regression checks.
- **Step 5: Document and Commit**: Update the session walkthrough and sync the telemetry logs for the engineering sector.

---

## 📚 Reference Material

# 2.3 Edit Tool Design

```python
class EditFileTool(Tool):
    """
    Precise file editing with conflict detection.
    Uses search/replace pattern for reliable edits.
    """

    name = "edit_file"
    description = "Edit a file by replacing specific content"

    def execute(
        self,
        path: str,
        search: str,
        replace: str,
        expected_occurrences: int = 1
    ) -> ToolResult:
        """
        Args:
            path: File to edit
            search: Exact text to find (must match exactly, including whitespace)
            replace: Text to replace with
            expected_occurrences: How many times search should appear (validation)
        """
        with open(path, 'r') as f:
            content = f.read()

        # Validate
        actual_occurrences = content.count(search)
        if actual_occurrences != expected_occurrences:
            return ToolResult(
                success=False,
                error=f"Expected {expected_occurrences} occurrences, found {actual_occurrences}"
            )

        if actual_occurrences == 0:
            return ToolResult(
                success=False,
                error="Search text not found in file"
            )

        # Apply edit
        new_content = content.replace(search, replace)

        with open(path, 'w') as f:
            f.write(new_content)

        return ToolResult(
            success=True,
            output=f"Replaced {actual_occurrences} occurrence(s)"
        )
```

---

## 3. Permission & Safety Patterns