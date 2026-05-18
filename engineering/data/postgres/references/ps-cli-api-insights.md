## 🛠️ Implementation SOP
Follow this step-by-step TDD procedure to execute the protocol:

- **Step 1: Baseline Context**: Verify the operational environment. Ensure required tools (like Python, Node, TS, or native CLI) are accessible before injecting new logic.
- **Step 2: Apply the Pattern**: Implement the core ps cli api insights logic directly into the active system context.
- **Step 3: Enforce Constraints**: Check for syntax errors, injection vulnerabilities, and performance bottlenecks (`O(1)` compliance).
- **Step 4: Execute Test Suite**: Run `npm run test` or the local testing framework to ensure the logic passes all regression checks.
- **Step 5: Document and Commit**: Update the session walkthrough and sync the telemetry logs for the engineering sector.

---

## 📚 Reference Material

---
title: CLI Query Insights API
description: CLI insights usage
tags: postgres, planetscale, cli, insights, query-patterns, api
---

# Query Insights via pscale CLI

Analyze slow queries and missing indexes using `pscale api`. Endpoints may change—see https://planetscale.com/docs/api/reference/getting-started-with-planetscale-api for current API docs.

## Using pscale api

The `pscale api` command makes authenticated API calls using your current login or service token (see [ps-cli-commands.md](ps-cli-commands.md#service-token-cicd) for auth setup). No need to manage auth headers manually.

```bash
pscale api "<endpoint>" [--method POST] [--field key=value] [--org <org>]
```

## Query Patterns Reports

```bash
# Create a new report
pscale api "organizations/{org}/databases/{db}/branches/{branch}/query-patterns-reports" \
  --method POST --org my-org

# Check status (poll until state=complete)
pscale api "organizations/{org}/databases/{db}/branches/{branch}/query-patterns-reports/{id}/status"

# Download completed report
pscale api "organizations/{org}/databases/{db}/branches/{branch}/query-patterns-reports/{id}"

# List all reports
pscale api "organizations/{org}/databases/{db}/branches/{branch}/query-patterns-reports"
```

## Schema Analysis

```bash
# Get branch schema
pscale api "organizations/{org}/databases/{db}/branches/{branch}/schema"

# Lint schema for issues
pscale api "organizations/{org}/databases/{db}/branches/{branch}/schema/lint"
```

## What to Look For

| Metric                           | Indicates             | Action                          |
| -------------------------------- | --------------------- | ------------------------------- |
| High `rows_read / rows_returned` | Missing or poor index | Add index on WHERE/JOIN columns |
| High `total_time_s`              | Heavy query           | Optimize or cache               |
| High `count` with same pattern   | N+1 queries           | Batch or eager-load             |
| `indexed: false`                 | Full table scan       | Add index                       |
