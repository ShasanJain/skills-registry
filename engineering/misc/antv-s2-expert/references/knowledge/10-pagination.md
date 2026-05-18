---
name: 10-pagination
description: Use when executing 10 pagination protocols within the engineering sector.
---

## 🛠️ Implementation SOP
Follow this step-by-step TDD procedure to execute the protocol:

- **Step 1: Baseline Context**: Verify the operational environment. Ensure required tools (like Python, Node, TS, or native CLI) are accessible before injecting new logic.
- **Step 2: Apply the Pattern**: Implement the core 10 pagination logic directly into the active system context.
- **Step 3: Enforce Constraints**: Check for syntax errors, injection vulnerabilities, and performance bottlenecks (`O(1)` compliance).
- **Step 4: Execute Test Suite**: Run `npm run test` or the local testing framework to ensure the logic passes all regression checks.
- **Step 5: Document and Commit**: Update the session walkthrough and sync the telemetry logs for the engineering sector.

---

## 📚 Reference Material

# Pagination

## Overview

S2 has built-in frontend pagination rendering. It handles data slicing internally but does **not** provide a pagination UI component — you need to implement or integrate one yourself (e.g., Ant Design's `Pagination` component).

## Configuration

Set the `pagination` property in `s2Options`:

```ts
const s2Options = {
  width: 600,
  height: 480,
  pagination: {
    pageSize: 4,   // rows per page
    current: 1,    // current page (1-based)
  },
};
```

## Pagination Type

| Property | Description | Type | Default | Required |
|---|---|---|---|---|
| `pageSize` | Number of rows per page | `number` | - | ✓ |
| `current` | Current page number (starts from 1) | `number` | `1` | ✓ |
| `total` | Total number of data items (read-only, set by S2 internally) | `number` | - | |

## React Integration Example

Combine S2's pagination config with a UI pagination component:

```tsx
import React, { useState } from 'react';
import { SheetComponent } from '@antv/s2-react';
import { Pagination } from 'antd';

function PaginatedTable({ dataCfg }) {
  const [current, setCurrent] = useState(1);
  const [pageSize, setPageSize] = useState(10);
  const [total, setTotal] = useState(0);

  const s2Options = {
    width: 600,
    height: 480,
    pagination: {
      pageSize,
      current,
    },
  };

  return (
    <div>
      <SheetComponent
        dataCfg={dataCfg}
        options={s2Options}
        onMounted={(instance) => {
          setTotal(instance.facet.viewCellHeights.getTotalLength());
        }}
      />
      <Pagination
        current={current}
        pageSize={pageSize}
        total={total}
        onChange={(page, size) => {
          setCurrent(page);
          setPageSize(size);
        }}
      />
    </div>
  );
}
```

## Vanilla JS Example

```ts
import { PivotSheet } from '@antv/s2';

const s2Options = {
  width: 600,
  height: 480,
  pagination: {
    pageSize: 5,
    current: 1,
  },
};

const s2 = new PivotSheet(container, s2DataConfig, s2Options);
await s2.render();

// Change page
function goToPage(page) {
  s2.updatePagination({
    current: page,
    pageSize: 5,
  });
  s2.render(false); // re-render without reinitializing
}
```

## Notes

- Pagination is **frontend-only** — all data is loaded upfront; S2 just renders the current page slice.
- For server-side pagination, manage `data` externally and update `s2DataConfig.data` when the page changes.
- The `total` field in pagination is typically read from the rendered result rather than set manually.
