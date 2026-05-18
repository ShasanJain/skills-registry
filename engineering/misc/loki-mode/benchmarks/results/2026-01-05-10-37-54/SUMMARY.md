---
name: SUMMARY
description: Use when executing summary protocols within the engineering sector.
---

## 🛠️ Implementation SOP
Follow this step-by-step TDD procedure to execute the protocol:

- **Step 1: Baseline Context**: Verify the operational environment. Ensure required tools (like Python, Node, TS, or native CLI) are accessible before injecting new logic.
- **Step 2: Apply the Pattern**: Implement the core summary logic directly into the active system context.
- **Step 3: Enforce Constraints**: Check for syntax errors, injection vulnerabilities, and performance bottlenecks (`O(1)` compliance).
- **Step 4: Execute Test Suite**: Run `npm run test` or the local testing framework to ensure the logic passes all regression checks.
- **Step 5: Document and Commit**: Update the session walkthrough and sync the telemetry logs for the engineering sector.

---

## 📚 Reference Material

# Loki Mode Benchmark Results

**Generated:** 2026-01-05 14:15:24

## Overview

This directory contains benchmark results for Loki Mode multi-agent system.

## Methodology

Loki Mode uses its multi-agent architecture to solve each problem:
1. **Architect Agent** analyzes the problem
2. **Engineer Agent** implements the solution
3. **QA Agent** validates with test cases
4. **Review Agent** checks code quality

This mirrors real-world software development more accurately than single-agent approaches.

## Running Benchmarks

```bash
# Setup only (download datasets)
./benchmarks/run-benchmarks.sh all

# Execute with Claude
./benchmarks/run-benchmarks.sh humaneval --execute
./benchmarks/run-benchmarks.sh humaneval --execute --limit 10  # First 10 only
./benchmarks/run-benchmarks.sh swebench --execute --limit 5    # First 5 only

# Use different model
./benchmarks/run-benchmarks.sh humaneval --execute --model opus
```
