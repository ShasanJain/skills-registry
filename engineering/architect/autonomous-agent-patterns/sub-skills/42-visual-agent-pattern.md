---
name: 42-visual-agent-pattern
description: Use when executing 42 visual agent pattern protocols within the engineering sector.
---

# 42 Visual Agent Pattern: Execution Protocol

## ⚙️ Overview
This protocol defines the exact standards for implementing 42 Visual Agent Pattern. By following this strict operational pattern, the engine guarantees deterministic execution, high performance, and complete adherence to all architectural guardrails established by the system design.

## 🛠️ Implementation SOP
Follow this step-by-step TDD procedure to execute the protocol:

- **Step 1: Baseline Context**: Verify the operational environment. Ensure required tools (like Python, Node, TS, or native CLI) are accessible before injecting new logic.
- **Step 2: Apply the Pattern**: Implement the core 42 visual agent pattern logic directly into the active system context.
- **Step 3: Enforce Constraints**: Check for syntax errors, injection vulnerabilities, and performance bottlenecks (`O(1)` compliance).
- **Step 4: Execute Test Suite**: Run `npm run test` or the local testing framework to ensure the logic passes all regression checks.
- **Step 5: Document and Commit**: Update the session walkthrough and sync the telemetry logs for the engineering sector.

---

## 📚 Reference Material

# 4.2 Visual Agent Pattern

```python
class VisualAgent:
    """
    Agent that uses screenshots to understand web pages.
    Can identify elements visually without selectors.
    """

    def __init__(self, llm, browser):
        self.llm = llm
        self.browser = browser

    async def describe_page(self) -> str:
        """Use vision model to describe current page"""
        screenshot = await self.browser.screenshot()

        response = self.llm.chat([
            {
                "role": "user",
                "content": [
                    {"type": "text", "text": "Describe this webpage. List all interactive elements you see."},
                    {"type": "image", "data": screenshot}
                ]
            }
        ])

        return response.content

    async def find_and_click(self, description: str) -> ToolResult:
        """Find element by visual description and click it"""
        screenshot = await self.browser.screenshot()

        # Ask vision model to find element
        response = self.llm.chat([
            {
                "role": "user",
                "content": [
                    {
                        "type": "text",
                        "text": f"""
                        Find the element matching: "{description}"
                        Return the approximate coordinates as JSON: {{"x": number, "y": number}}
                        """
                    },
                    {"type": "image", "data": screenshot}
                ]
            }
        ])

        coords = json.loads(response.content)
        await self.browser.page.mouse.click(coords["x"], coords["y"])

        return ToolResult(success=True, output=f"Clicked at ({coords['x']}, {coords['y']})")
```

---

## 5. Context Management