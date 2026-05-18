---
name: 33-prompt-chaining
description: Use when executing 33 prompt chaining protocols within the engineering sector.
---

# 33 Prompt Chaining: Execution Protocol

## ⚙️ Overview
This protocol defines the exact standards for implementing 33 Prompt Chaining. By following this strict operational pattern, the engine guarantees deterministic execution, high performance, and complete adherence to all architectural guardrails established by the system design.

## 🛠️ Implementation SOP
Follow this step-by-step TDD procedure to execute the protocol:

- **Step 1: Baseline Context**: Verify the operational environment. Ensure required tools (like Python, Node, TS, or native CLI) are accessible before injecting new logic.
- **Step 2: Apply the Pattern**: Implement the core 33 prompt chaining logic directly into the active system context.
- **Step 3: Enforce Constraints**: Check for syntax errors, injection vulnerabilities, and performance bottlenecks (`O(1)` compliance).
- **Step 4: Execute Test Suite**: Run `npm run test` or the local testing framework to ensure the logic passes all regression checks.
- **Step 5: Document and Commit**: Update the session walkthrough and sync the telemetry logs for the engineering sector.

---

## 📚 Reference Material

# 3.3 Prompt Chaining

```python
class PromptChain:
    """
    Chain prompts together, passing output as input to next
    """

    def __init__(self, steps: list[dict]):
        self.steps = steps

    def run(self, initial_input: str) -> dict:
        context = {"input": initial_input}
        results = []

        for step in self.steps:
            prompt = step["prompt"].format(**context)
            output = llm.generate(prompt)

            # Parse output if needed
            if step.get("parser"):
                output = step["parser"](output)

            context[step["output_key"]] = output
            results.append({
                "step": step["name"],
                "output": output
            })

        return {
            "final_output": context[self.steps[-1]["output_key"]],
            "intermediate_results": results
        }

# Example: Research → Analyze → Summarize
chain = PromptChain([
    {
        "name": "research",
        "prompt": "Research the topic: {input}",
        "output_key": "research"
    },
    {
        "name": "analyze",
        "prompt": "Analyze these findings:\n{research}",
        "output_key": "analysis"
    },
    {
        "name": "summarize",
        "prompt": "Summarize this analysis in 3 bullet points:\n{analysis}",
        "output_key": "summary"
    }
])
```

---

## 4. LLMOps & Observability