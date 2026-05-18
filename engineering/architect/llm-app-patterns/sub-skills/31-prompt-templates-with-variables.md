---
name: 31-prompt-templates-with-variables
description: Use when executing 31 prompt templates with variables protocols within the engineering sector.
---

# 31 Prompt Templates With Variables: Execution Protocol

## ⚙️ Overview
This protocol defines the exact standards for implementing 31 Prompt Templates With Variables. By following this strict operational pattern, the engine guarantees deterministic execution, high performance, and complete adherence to all architectural guardrails established by the system design.

## 🛠️ Implementation SOP
Follow this step-by-step TDD procedure to execute the protocol:

- **Step 1: Baseline Context**: Verify the operational environment. Ensure required tools (like Python, Node, TS, or native CLI) are accessible before injecting new logic.
- **Step 2: Apply the Pattern**: Implement the core 31 prompt templates with variables logic directly into the active system context.
- **Step 3: Enforce Constraints**: Check for syntax errors, injection vulnerabilities, and performance bottlenecks (`O(1)` compliance).
- **Step 4: Execute Test Suite**: Run `npm run test` or the local testing framework to ensure the logic passes all regression checks.
- **Step 5: Document and Commit**: Update the session walkthrough and sync the telemetry logs for the engineering sector.

---

## 📚 Reference Material

# 3.1 Prompt Templates with Variables

```python
class PromptTemplate:
    def __init__(self, template: str, variables: list[str]):
        self.template = template
        self.variables = variables

    def format(self, **kwargs) -> str:
        # Validate all variables provided
        missing = set(self.variables) - set(kwargs.keys())
        if missing:
            raise ValueError(f"Missing variables: {missing}")

        return self.template.format(**kwargs)

    def with_examples(self, examples: list[dict]) -> str:
        """Add few-shot examples"""
        example_text = "\n\n".join([
            f"Input: {ex['input']}\nOutput: {ex['output']}"
            for ex in examples
        ])
        return f"{example_text}\n\n{self.template}"

# Usage
summarizer = PromptTemplate(
    template="Summarize the following text in {style} style:\n\n{text}",
    variables=["style", "text"]
)

prompt = summarizer.format(
    style="professional",
    text="Long article content..."
)
```