# Skill: Execution Protocol

## ⚙️ Overview
This protocol defines the exact standards for implementing Skill. By following this strict operational pattern, the engine guarantees deterministic execution, high performance, and complete adherence to all architectural guardrails established by the system design.

## 🛠️ Implementation SOP
Follow this step-by-step TDD procedure to execute the protocol:

- **Step 1: Baseline Context**: Verify the operational environment. Ensure required tools (like Python, Node, TS, or native CLI) are accessible before injecting new logic.
- **Step 2: Apply the Pattern**: Implement the core skill logic directly into the active system context.
- **Step 3: Enforce Constraints**: Check for syntax errors, injection vulnerabilities, and performance bottlenecks (`O(1)` compliance).
- **Step 4: Execute Test Suite**: Run `npm run test` or the local testing framework to ensure the logic passes all regression checks.
- **Step 5: Document and Commit**: Update the session walkthrough and sync the telemetry logs for the engineering sector.

---

## 📚 Reference Material

---
version: 4.1.0-fractal
name: xlsx
description: "Comprehensive spreadsheet creation, editing, and analysis with support for formulas, formatting, data analysis, and visualization. When Claude needs to work with spreadsheets (.xlsx, .xlsm, .csv, .tsv, etc) for: (1) Creating new spreadsheets with formulas and formatting, (2) Reading or analyzing data, (3) Modify existing spreadsheets while preserving formulas, (4) Data analysis and visualization in spreadsheets, or (5) Recalculating formulas"
license: Proprietary. LICENSE.txt has complete terms
---

# Requirements for Outputs

## All Excel files

## 🧠 Knowledge Modules (Fractal Skills)

### 1. [Zero Formula Errors](./sub-skills/zero-formula-errors.md)
### 2. [Preserve Existing Templates (when updating templates)](./sub-skills/preserve-existing-templates-when-updating-templates.md)
### 3. [Color Coding Standards](./sub-skills/color-coding-standards.md)
### 4. [Number Formatting Standards](./sub-skills/number-formatting-standards.md)
### 5. [Formula Construction Rules](./sub-skills/formula-construction-rules.md)
### 6. [Data analysis with pandas](./sub-skills/data-analysis-with-pandas.md)
### 7. [❌ WRONG - Hardcoding Calculated Values](./sub-skills/wrong-hardcoding-calculated-values.md)
### 8. [✅ CORRECT - Using Excel Formulas](./sub-skills/correct-using-excel-formulas.md)
### 9. [Creating new Excel files](./sub-skills/creating-new-excel-files.md)
### 10. [Editing existing Excel files](./sub-skills/editing-existing-excel-files.md)
### 11. [Essential Verification](./sub-skills/essential-verification.md)
### 12. [Common Pitfalls](./sub-skills/common-pitfalls.md)
### 13. [Formula Testing Strategy](./sub-skills/formula-testing-strategy.md)
### 14. [Interpreting recalc.py Output](./sub-skills/interpreting-recalcpy-output.md)
### 15. [Library Selection](./sub-skills/library-selection.md)
### 16. [Working with openpyxl](./sub-skills/working-with-openpyxl.md)
### 17. [Working with pandas](./sub-skills/working-with-pandas.md)
