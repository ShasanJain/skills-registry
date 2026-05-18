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
name: docx
description: "Comprehensive document creation, editing, and analysis with support for tracked changes, comments, formatting preservation, and text extraction. When Claude needs to work with professional documents (.docx files) for: (1) Creating new documents, (2) Modifying or editing content, (3) Working with tracked changes, (4) Adding comments, or any other document tasks"
license: Proprietary. LICENSE.txt has complete terms
---

# DOCX creation, editing, and analysis

## Overview

A user may ask you to create, edit, or analyze the contents of a .docx file. A .docx file is essentially a ZIP archive containing XML files and other resources that you can read or edit. You have different tools and workflows available for different tasks.

## Workflow Decision Tree

## 🧠 Knowledge Modules (Fractal Skills)

### 1. [Reading/Analyzing Content](./sub-skills/readinganalyzing-content.md)
### 2. [Creating New Document](./sub-skills/creating-new-document.md)
### 3. [Editing Existing Document](./sub-skills/editing-existing-document.md)
### 4. [Text extraction](./sub-skills/text-extraction.md)
### 5. [Raw XML access](./sub-skills/raw-xml-access.md)
### 6. [Workflow](./sub-skills/workflow.md)
### 7. [Workflow](./sub-skills/workflow.md)
### 8. [Tracked changes workflow](./sub-skills/tracked-changes-workflow.md)
