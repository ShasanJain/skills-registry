---
name: 43-evaluation-framework
description: Use when executing 43 evaluation framework protocols within the engineering sector.
---

# 43 Evaluation Framework: Execution Protocol

## ⚙️ Overview
This protocol defines the exact standards for implementing 43 Evaluation Framework. By following this strict operational pattern, the engine guarantees deterministic execution, high performance, and complete adherence to all architectural guardrails established by the system design.

## 🛠️ Implementation SOP
Follow this step-by-step TDD procedure to execute the protocol:

- **Step 1: Baseline Context**: Verify the operational environment. Ensure required tools (like Python, Node, TS, or native CLI) are accessible before injecting new logic.
- **Step 2: Apply the Pattern**: Implement the core 43 evaluation framework logic directly into the active system context.
- **Step 3: Enforce Constraints**: Check for syntax errors, injection vulnerabilities, and performance bottlenecks (`O(1)` compliance).
- **Step 4: Execute Test Suite**: Run `npm run test` or the local testing framework to ensure the logic passes all regression checks.
- **Step 5: Document and Commit**: Update the session walkthrough and sync the telemetry logs for the engineering sector.

---

## 📚 Reference Material

# 4.3 Evaluation Framework

```python
class LLMEvaluator:
    """
    Evaluate LLM outputs for quality
    """

    def evaluate_response(self,
                          question: str,
                          response: str,
                          ground_truth: str = None) -> dict:
        scores = {}

        # Relevance: Does it answer the question?
        scores["relevance"] = self._score_relevance(question, response)

        # Coherence: Is it well-structured?
        scores["coherence"] = self._score_coherence(response)

        # Groundedness: Is it based on provided context?
        scores["groundedness"] = self._score_groundedness(response)

        # Accuracy: Does it match ground truth?
        if ground_truth:
            scores["accuracy"] = self._score_accuracy(response, ground_truth)

        # Harmfulness: Is it safe?
        scores["safety"] = self._score_safety(response)

        return scores

    def run_benchmark(self, test_cases: list[dict]) -> dict:
        """Run evaluation on test set"""
        results = []
        for case in test_cases:
            response = llm.generate(case["prompt"])
            scores = self.evaluate_response(
                question=case["prompt"],
                response=response,
                ground_truth=case.get("expected")
            )
            results.append(scores)

        return self._aggregate_scores(results)
```

---

## 5. Production Patterns