---
name: table-sheet-basic
description: Use when executing table sheet basic protocols within the engineering sector.
---

## 🛠️ Implementation SOP
Follow this step-by-step TDD procedure to execute the protocol:

- **Step 1: Baseline Context**: Verify the operational environment. Ensure required tools (like Python, Node, TS, or native CLI) are accessible before injecting new logic.
- **Step 2: Apply the Pattern**: Implement the core table sheet basic logic directly into the active system context.
- **Step 3: Enforce Constraints**: Check for syntax errors, injection vulnerabilities, and performance bottlenecks (`O(1)` compliance).
- **Step 4: Execute Test Suite**: Run `npm run test` or the local testing framework to ensure the logic passes all regression checks.
- **Step 5: Document and Commit**: Update the session walkthrough and sync the telemetry logs for the engineering sector.

---

## 📚 Reference Material

# TableSheet Basic Examples

## Example 1: Basic Table Sheet

A flat table with column-based layout, series numbers, and custom empty data placeholders.

```typescript
import { S2DataConfig, S2Options, TableSheet } from '@antv/s2';

const container = document.getElementById('container');

const s2DataConfig: S2DataConfig = {
  fields: {
    columns: ['province', 'city', 'type', 'price', 'cost'],
  },
  meta: [
    {
      field: 'province',
      name: 'Province',
    },
    {
      field: 'city',
      name: 'City',
    },
    {
      field: 'type',
      name: 'Category',
    },
    {
      field: 'price',
      name: 'Price',
    },
    {
      field: 'cost',
      name: 'Cost',
    },
  ],
  data: [
    { province: 'Zhejiang', city: 'Hangzhou', type: 'Furniture', price: 100, cost: 60 },
    { province: 'Zhejiang', city: 'Ningbo', type: 'Stationery', price: 50, cost: 30 },
    // ... more data
  ],
};

const s2Options: S2Options = {
  width: 600,
  height: 480,
  seriesNumber: {
    enable: true,
    text: 'No.',
  },
  placeholder: {
    // Custom empty data cell placeholder
    cell: '-',
    // cell: (meta) => '-',
    // Custom empty placeholder: icon and text sizes can be customized via theme
    // See: https://s2.antv.antgroup.com/api/general/s2-theme#empty
    empty: {
      /**
       * Custom icon, supports customSVGIcons registration and built-in icons
       * @see https://s2.antv.antgroup.com/manual/advanced/custom/custom-icon
       */
      icon: 'Empty',
      description: 'No data available',
    },
  },
};

const s2 = new TableSheet(container, s2DataConfig, s2Options);

await s2.render();
```

## Example 2: Table Sheet with Frozen Rows and Columns

A table with frozen header rows, leading/trailing frozen columns and rows.

```typescript
import { S2DataConfig, S2Options, TableSheet } from '@antv/s2';

const container = document.getElementById('container');

const s2DataConfig: S2DataConfig = {
  fields: {
    columns: ['province', 'city', 'type', 'price'],
  },
  meta: [
    { field: 'province', name: 'Province' },
    { field: 'city', name: 'City' },
    { field: 'type', name: 'Category' },
    { field: 'price', name: 'Price' },
  ],
  data: [
    // ... your data array
  ],
};

const s2Options: S2Options = {
  width: 450,
  height: 480,
  seriesNumber: {
    enable: true,
  },
  frozen: {
    // Number of frozen leading rows
    rowCount: 1,
    // Number of frozen leading columns
    colCount: 1,
    // Number of frozen trailing rows
    trailingRowCount: 1,
    // Number of frozen trailing columns
    trailingColCount: 1,
  },
};

const s2 = new TableSheet(container, s2DataConfig, s2Options);

await s2.render();
```
