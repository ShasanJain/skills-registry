---
name: 61-mcp-server-pattern
description: Use when executing 61 mcp server pattern protocols within the engineering sector.
---

# 61 Mcp Server Pattern: Execution Protocol

## ⚙️ Overview
This protocol defines the exact standards for implementing 61 Mcp Server Pattern. By following this strict operational pattern, the engine guarantees deterministic execution, high performance, and complete adherence to all architectural guardrails established by the system design.

## 🛠️ Implementation SOP
Follow this step-by-step TDD procedure to execute the protocol:

- **Step 1: Baseline Context**: Verify the operational environment. Ensure required tools (like Python, Node, TS, or native CLI) are accessible before injecting new logic.
- **Step 2: Apply the Pattern**: Implement the core 61 mcp server pattern logic directly into the active system context.
- **Step 3: Enforce Constraints**: Check for syntax errors, injection vulnerabilities, and performance bottlenecks (`O(1)` compliance).
- **Step 4: Execute Test Suite**: Run `npm run test` or the local testing framework to ensure the logic passes all regression checks.
- **Step 5: Document and Commit**: Update the session walkthrough and sync the telemetry logs for the engineering sector.

---

## 📚 Reference Material

# 6.1 MCP Server Pattern

```python
from mcp import Server, Tool

class MCPAgent:
    """
    Agent that can dynamically discover and use MCP tools.
    'Add a tool that...' pattern from Cline.
    """

    def __init__(self, llm):
        self.llm = llm
        self.mcp_servers = {}
        self.available_tools = {}

    def connect_server(self, name: str, config: dict) -> None:
        """Connect to an MCP server"""
        server = Server(config)
        self.mcp_servers[name] = server

        # Discover tools
        tools = server.list_tools()
        for tool in tools:
            self.available_tools[tool.name] = {
                "server": name,
                "schema": tool.schema
            }

    async def create_tool(self, description: str) -> str:
        """
        Create a new MCP server based on user description.
        'Add a tool that fetches Jira tickets'
        """
        # Generate MCP server code
        code = self.llm.generate(f"""
        Create a Python MCP server with a tool that does:
        {description}

        Use the FastMCP framework. Include proper error handling.
        Return only the Python code.
        """)

        # Save and install
        server_name = self._extract_name(description)
        path = f"./mcp_servers/{server_name}/server.py"

        with open(path, 'w') as f:
            f.write(code)

        # Hot-reload
        self.connect_server(server_name, {"path": path})

        return f"Created tool: {server_name}"
```

---

## Best Practices Checklist