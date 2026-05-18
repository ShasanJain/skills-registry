---
name: 13-frozen
description: Use when executing 13 frozen protocols within the engineering sector.
---

## 🛠️ Implementation SOP
Follow this step-by-step TDD procedure to execute the protocol:

- **Step 1: Baseline Context**: Verify the operational environment. Ensure required tools (like Python, Node, TS, or native CLI) are accessible before injecting new logic.
- **Step 2: Apply the Pattern**: Implement the core 13 frozen logic directly into the active system context.
- **Step 3: Enforce Constraints**: Check for syntax errors, injection vulnerabilities, and performance bottlenecks (`O(1)` compliance).
- **Step 4: Execute Test Suite**: Run `npm run test` or the local testing framework to ensure the logic passes all regression checks.
- **Step 5: Document and Commit**: Update the session walkthrough and sync the telemetry logs for the engineering sector.

---

## 📚 Reference Material

# Frozen Rows and Columns

## Overview

The frozen (freeze) feature pins specific rows and columns so they remain visible while scrolling. This is configured via the `s2Options.frozen` property.

## Frozen Configuration

| Property | Type | Default | Description |
|----------|------|---------|-------------|
| rowHeader | `boolean \| number` | `true` | Freeze row header. When `number`, sets the max frozen area ratio (0, 1) — 0 means no freeze. When `boolean`, `true` = 0.5, `false` = 0. **Pivot table only.** |
| rowCount | `number` | `0` | Number of frozen rows from the **top**, counted by leaf nodes. (Not effective in pivot tables with row serial number enabled and custom serial number cells.) |
| colCount | `number` | `0` | Number of frozen columns from the **left**, counted by leaf nodes. |
| trailingRowCount | `number` | `0` | Number of frozen rows from the **bottom**, counted by leaf nodes. (Not effective in pivot tables with row serial number enabled and custom serial number cells.) |
| trailingColCount | `number` | `0` | Number of frozen columns from the **right**, counted by leaf nodes. |

## Usage

### Freeze Row Header (Pivot Table)

```ts
const s2Options = {
  frozen: {
    rowHeader: true,   // Freeze row header with default 0.5 ratio
  },
};

// Or set a custom ratio
const s2Options = {
  frozen: {
    rowHeader: 0.3,    // Row header takes at most 30% of table width
  },
};
```

### Freeze Rows and Columns (Table Sheet)

```ts
const s2Options = {
  frozen: {
    colCount: 2,            // Freeze first 2 columns
    trailingColCount: 1,    // Freeze last 1 column
    rowCount: 3,            // Freeze first 3 rows
    trailingRowCount: 2,    // Freeze last 2 rows
  },
};
```

### Freeze Only Columns

```ts
const s2Options = {
  frozen: {
    colCount: 1,            // Freeze first column
    trailingColCount: 1,    // Freeze last column
  },
};
```

## Notes

- Row/column counts are based on **leaf nodes** in the hierarchy.
- For pivot tables, `rowHeader` controls the row header area freeze. Use `rowCount`/`trailingRowCount` for data row freezing.
- Setting `rowHeader: false` or `rowHeader: 0` disables row header freezing in pivot tables.
