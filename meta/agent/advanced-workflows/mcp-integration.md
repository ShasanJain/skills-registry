# MCP Integration: Model Context Protocol Connectivity

The Model Context Protocol (MCP) is the 2026 industry standard for dynamic tool integration. Instead of writing custom python scripts for every API, the engine seamlessly connects to standardized MCP servers (e.g., GitHub, SQLite, FileSystem) to interact with external data environments securely and efficiently.

## ⚙️ MCP Connection SOP

Follow this step-by-step procedure to manage MCP tool integrations:

- **Step 1: Identify Required Capabilities**: Determine if the current task requires external tool access (e.g., querying an SQLite database, interacting with a remote GitHub repository, or reading the local FileSystem).
- **Step 2: Scan Available MCP Servers**: Use the global context or initialization list to check which MCP servers are currently active and available to the agent session.
- **Step 3: Call Server Resources**: Execute the exact required tools exposed by the MCP server (e.g., `mcp_github-mcp-server_search_code` or `mcp_sqlite_query`). 
- **Step 4: Parse Standardized Outputs**: Read the JSON or structured text returned by the MCP endpoint. Never assume the shape of the data; parse it strictly according to the defined response schema.
- **Step 5: Handle Protocol Errors**: If an MCP connection fails or a tool returns an unauthorized error, do not brute-force the call. Log the failure and request human-in-the-loop (HITL) authentication.
- **Step 6: Document Integration Trace**: Note the MCP tools utilized and data retrieved within the final walkthrough artifact.
