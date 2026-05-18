---
name: 06-data-config
description: Use when executing 06 data config protocols within the engineering sector.
---

## 🛠️ Implementation SOP
Follow this step-by-step TDD procedure to execute the protocol:

- **Step 1: Baseline Context**: Verify the operational environment. Ensure required tools (like Python, Node, TS, or native CLI) are accessible before injecting new logic.
- **Step 2: Apply the Pattern**: Implement the core 06 data config logic directly into the active system context.
- **Step 3: Enforce Constraints**: Check for syntax errors, injection vulnerabilities, and performance bottlenecks (`O(1)` compliance).
- **Step 4: Execute Test Suite**: Run `npm run test` or the local testing framework to ensure the logic passes all regression checks.
- **Step 5: Document and Commit**: Update the session walkthrough and sync the telemetry logs for the engineering sector.

---

## 📚 Reference Material

# S2DataConfig — Data Configuration

## Overview

`S2DataConfig` defines the data source and field mappings for S2 tables. It includes raw data, field dimensions, metadata for formatting/naming, sort parameters, and filter parameters.

```ts
const s2DataConfig = {
  data: [],
  fields: {
    rows: [],
    columns: [],
    values: [],
  },
  meta: [],
  sortParams: [],
  filterParams: [],
};
```

## Top-Level Properties

| Property | Description | Type | Required |
|---|---|---|---|
| `data` | Raw data array | `RawData[]` | ✓ |
| `fields` | Dimension/measure field mapping | `Fields` | ✓ |
| `meta` | Field metadata (aliases, formatting) | `Meta[]` | |
| `sortParams` | Sort configuration | `SortParam[]` | |
| `filterParams` | Filter configuration (detail table only) | `FilterParam[]` | |

## Fields

Configures which data fields map to rows, columns, and values (measures).

| Property | Description | Type | Default |
|---|---|---|---|
| `rows` | Row dimensions (can use custom tree nodes) | `string[]` \| `CustomTreeNode[]` | `[]` |
| `columns` | Column dimensions (can use custom tree nodes) | `string[]` \| `CustomTreeNode[]` | `[]` |
| `values` | Measure/value fields | `string[]` | `[]` |
| `valueInCols` | Whether values appear in column headers | `boolean` | `true` |
| `customValueOrder` | Custom order of values in row/column hierarchy (0-based index) | `number` | - |

### Example

```ts
const s2DataConfig = {
  data: [
    { province: 'Zhejiang', city: 'Hangzhou', type: 'Furniture', price: 100 },
    { province: 'Zhejiang', city: 'Ningbo', type: 'Furniture', price: 200 },
  ],
  fields: {
    rows: ['province', 'city'],
    columns: ['type'],
    values: ['price'],
    valueInCols: true, // values displayed in column headers (default)
  },
};
```

## Meta

Field metadata for configuring display names and value formatting. Applies to row headers, column headers, and data cells (corner cells do not support formatting).

| Property | Description | Type | Required |
|---|---|---|---|
| `field` | Field ID (matches fields in `Fields`). Supports string, string array, or RegExp. | `string \| string[] \| RegExp` | |
| `name` | Display name (alias) for the field | `string` | |
| `description` | Field description, shown in tooltips for row/col headers and cells | `string` | |
| `formatter` | Formatting function. For text fields: used for enum aliases. For numeric fields: used for unit formatting. Second parameter (`data`) exists only for data cells. | `(value, data?, meta?) => string` | |
| `renderer` | Cell render type (image, video, etc.) | `Renderer` | |

### Formatter Function Signature

```ts
formatter: (
  value: unknown,
  data?: Data | Data[],   // only for data cells; array when multiple cells selected in tooltip
  meta?: Node | ViewMeta
) => string
```

### Example

```ts
const s2DataConfig = {
  data: [...],
  fields: {
    rows: ['province', 'city'],
    columns: ['type'],
    values: ['price'],
  },
  meta: [
    {
      field: 'province',
      name: 'Province',  // display alias
    },
    {
      field: 'city',
      name: 'City',
    },
    {
      field: 'price',
      name: 'Price',
      description: 'Total sales price',
      formatter: (value) => `$${Number(value).toFixed(2)}`,
    },
    {
      // Match multiple fields with array
      field: ['type'],
      name: 'Category',
    },
  ],
};
```

### Renderer

For rendering images or videos in cells:

| Property | Description | Type | Default |
|---|---|---|---|
| `type` | Render type | `'IMAGE' \| 'VIDEO'` | (required) |
| `clickToPreview` | Enable click-to-preview for images/videos | `boolean` | `true` |
| `fallback` | Fallback text if image/video fails to load | `string` | |
| `timeout` | Load timeout in milliseconds | `number` | `10000` |

## FilterParam (Detail Table Only)

| Property | Description | Type | Required |
|---|---|---|---|
| `filterKey` | Field ID to filter on | `string` | ✓ |
| `filteredValues` | Values to exclude | `unknown[]` | |
| `customFilter` | Custom filter function. Final result: passes `customFilter` AND not in `filteredValues`. | `(raw: Record<string, string>) => boolean` | |

### Example

```ts
const s2DataConfig = {
  data: [...],
  fields: { columns: ['province', 'city', 'price'] },
  filterParams: [
    {
      filterKey: 'province',
      filteredValues: ['Zhejiang'],
    },
    {
      filterKey: 'city',
      customFilter: (row) => row.city !== 'Hangzhou',
    },
  ],
};
```
