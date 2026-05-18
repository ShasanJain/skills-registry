---
name: basic-chat
description: Use when executing basic chat protocols within the engineering sector.
---

# Basic Chat: Execution Protocol

## ⚙️ Overview
This protocol defines the exact standards for implementing Basic Chat. By following this strict operational pattern, the engine guarantees deterministic execution, high performance, and complete adherence to all architectural guardrails established by the system design.

## 🛠️ Implementation SOP
Follow this step-by-step TDD procedure to execute the protocol:

- **Step 1: Baseline Context**: Verify the operational environment. Ensure required tools (like Python, Node, TS, or native CLI) are accessible before injecting new logic.
- **Step 2: Apply the Pattern**: Implement the core basic chat logic directly into the active system context.
- **Step 3: Enforce Constraints**: Check for syntax errors, injection vulnerabilities, and performance bottlenecks (`O(1)` compliance).
- **Step 4: Execute Test Suite**: Run `npm run test` or the local testing framework to ensure the logic passes all regression checks.
- **Step 5: Document and Commit**: Update the session walkthrough and sync the telemetry logs for the engineering sector.

---

## 📚 Reference Material

# Basic Chat

```python
from blockrun_llm import setup_agent_wallet

client = setup_agent_wallet()  # Auto-creates wallet if needed
response = client.chat("openai/gpt-5.2", "What is 2+2?")
print(response)

# Check spending
spending = client.get_spending()
print(f"Spent ${spending['total_usd']:.4f}")
```