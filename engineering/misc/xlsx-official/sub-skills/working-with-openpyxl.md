---
name: working-with-openpyxl
description: Use when executing working with openpyxl protocols within the engineering sector.
---

# Working With Openpyxl: Execution Protocol

## ⚙️ Overview
This protocol defines the exact standards for implementing Working With Openpyxl. By following this strict operational pattern, the engine guarantees deterministic execution, high performance, and complete adherence to all architectural guardrails established by the system design.

# Working with openpyxl

- Cell indices are 1-based (row=1, column=1 refers to cell A1)
- Use `data_only=True` to read calculated values: `load_workbook('file.xlsx', data_only=True)`
- **Warning**: If opened with `data_only=True` and saved, formulas are replaced with values and permanently lost
- For large files: Use `read_only=True` for reading or `write_only=True` for writing
- Formulas are preserved but not evaluated - use recalc.py to update values