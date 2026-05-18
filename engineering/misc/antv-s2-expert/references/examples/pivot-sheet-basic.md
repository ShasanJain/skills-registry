---
name: pivot-sheet-basic
description: Use when executing pivot sheet basic protocols within the engineering sector.
---

## 🛠️ Implementation SOP
Follow this step-by-step TDD procedure to execute the protocol:

- **Step 1: Baseline Context**: Verify the operational environment. Ensure required tools (like Python, Node, TS, or native CLI) are accessible before injecting new logic.
- **Step 2: Apply the Pattern**: Implement the core pivot sheet basic logic directly into the active system context.
- **Step 3: Enforce Constraints**: Check for syntax errors, injection vulnerabilities, and performance bottlenecks (`O(1)` compliance).
- **Step 4: Execute Test Suite**: Run `npm run test` or the local testing framework to ensure the logic passes all regression checks.
- **Step 5: Document and Commit**: Update the session walkthrough and sync the telemetry logs for the engineering sector.

---

## 📚 Reference Material

# PivotSheet Basic Examples

## Example 1: Grid Mode PivotSheet

A basic pivot table with grid layout, rows/columns/values configuration, and meta field aliases.

```typescript
import { PivotSheet, S2DataConfig, S2Options } from '@antv/s2';

const container = document.getElementById('container');

const s2DataConfig: S2DataConfig = {
  fields: {
    rows: ['province', 'city'],
    columns: ['type', 'sub_type'],
    values: ['number'],
  },
  meta: [
    // Supports batch setting or regex matching:
    // field: ['province', 'city'],
    // field: /type/,
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
      field: 'sub_type',
      name: 'Sub Category',
    },
    {
      field: 'number',
      name: 'Quantity',
      // Custom formatter:
      // formatter: (value, record, meta) => {
      //   return `${value / 100} %`;
      // },
    },
  ],
  data: [
    { province: 'Zhejiang', city: 'Hangzhou', type: 'Furniture', sub_type: 'Table', number: 7789 },
    { province: 'Zhejiang', city: 'Hangzhou', type: 'Furniture', sub_type: 'Sofa', number: 2367 },
    // ... more data
  ],
};

const s2Options: S2Options = {
  width: 600,
  height: 480,
  hierarchyType: 'grid',
  // Custom corner extra field text when values are on row header (default: "Values")
  cornerExtraFieldText: 'Metrics',
  interaction: {
    copy: {
      enable: true,
      withFormat: true,
      withHeader: true,
    },
  },
  // Show series number column:
  // seriesNumber: {
  //   enable: true,
  //   text: 'No.',
  // },
  frozen: {
    // Row header is frozen by default; both row header and data area show scrollbars
    // rowHeader: false,
    // When row header is frozen, row header width is 1/2 of table, supports dynamic adjustment (0 - 1)
    // rowHeader: 0.2,
  },
};

const s2 = new PivotSheet(container, s2DataConfig, s2Options);

await s2.render();
```

## Example 2: Tree Mode PivotSheet

A pivot table with tree hierarchy layout, supporting expand/collapse of row dimensions.

```typescript
import { PivotSheet, S2Options } from '@antv/s2';

const container = document.getElementById('container');

const s2Options: S2Options = {
  width: 600,
  height: 480,
  hierarchyType: 'tree',

  // Custom corner text (default: "Dimension1/Dimension2")
  // cornerText: 'Metrics',

  // Show series number:
  // seriesNumber: {
  //   enable: true,
  //   text: 'No.',
  // },
  style: {
    rowCell: {
      // Custom tree mode row header width:
      // width: 80,

      // Collapse all:
      // collapseAll: true,

      // Collapse all cities under Zhejiang province
      collapseFields: {
        'root[&]Zhejiang': true,
      },
    },
  },
  frozen: {
    // Row header is frozen by default
    // rowHeader: false,
    // When frozen, row header width ratio (0 - 1)
    // rowHeader: 0.2,
  },
};

const s2 = new PivotSheet(container, dataCfg, s2Options);

await s2.render();
```

## Example 3: Grid-Tree Mode with Totals

Grid-tree mode combines flat layout with expand/collapse. Each dimension level has its own column while supporting expand/collapse of child nodes.

```typescript
import { PivotSheet, S2Options, setLang } from '@antv/s2';

const container = document.getElementById('container');

const s2Options: S2Options = {
  width: 1200,
  height: 800,
  // Grid-tree mode: flat layout + expand/collapse
  hierarchyType: 'grid-tree',
  style: {
    rowCell: {
      // Default expand to level 1 (starting from 0)
      expandDepth: 1,
    },
  },
  // Configure grand totals and subtotals
  totals: {
    row: {
      showGrandTotals: true,
      showSubTotals: true,
      subTotalsDimensions: ['province'],
      grandTotalsLabel: 'Grand Total',
      subTotalsLabel: 'Subtotal',
      // Auto-calculate subtotals and grand totals
      calcSubTotals: {
        aggregation: 'SUM',
      },
      calcGrandTotals: {
        aggregation: 'SUM',
      },
      reverseSubTotalsLayout: true,
    },
  },
};

setLang('en_US');

const s2 = new PivotSheet(container, dataCfg, s2Options);

await s2.render();
```
