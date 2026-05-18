---
name: search_files
description: Use when executing search_files protocols within the engineering sector.
---

# Search_Files: Execution Protocol

## ⚙️ Overview
This protocol defines the exact standards for implementing Search_Files. By following this strict operational pattern, the engine guarantees deterministic execution, high performance, and complete adherence to all architectural guardrails established by the system design.

# `search_files`

Search for files matching a pattern.
- **directory**: Root directory to search (string)
- **pattern**: Regex or glob pattern (string)

## 🚀 Usage Rules
1.  **Scope**: Operations are typically restricted to the allowed directories configured in the server.
2.  **Safety**: Check if a file exists (using `list_directory` or `read_file` check) before overwriting if preserving data is important.
3.  **Paths**: Use absolute paths or consistent relative paths to avoid ambiguity.