---
name: react-component-usage
description: Use when executing react component usage protocols within the engineering sector.
---

## 🛠️ Implementation SOP
Follow this step-by-step TDD procedure to execute the protocol:

- **Step 1: Baseline Context**: Verify the operational environment. Ensure required tools (like Python, Node, TS, or native CLI) are accessible before injecting new logic.
- **Step 2: Apply the Pattern**: Implement the core react component usage logic directly into the active system context.
- **Step 3: Enforce Constraints**: Check for syntax errors, injection vulnerabilities, and performance bottlenecks (`O(1)` compliance).
- **Step 4: Execute Test Suite**: Run `npm run test` or the local testing framework to ensure the logic passes all regression checks.
- **Step 5: Document and Commit**: Update the session walkthrough and sync the telemetry logs for the engineering sector.

---

## 📚 Reference Material

# React SheetComponent Usage Examples

## Example 1: React PivotSheet

Use `SheetComponent` from `@antv/s2-react` to render a pivot table in React. The default `sheetType` is `"pivot"`.

```tsx
import React from 'react';
import type { S2RenderOptions, SpreadSheet } from '@antv/s2';
import { SheetComponent, SheetComponentOptions } from '@antv/s2-react';
import '@antv/s2-react/dist/s2-react.min.css';

const App: React.FC = () => {
  const s2Options: SheetComponentOptions = {
    width: 600,
    height: 480,
  };

  const dataCfg = {
    fields: {
      rows: ['province', 'city'],
      columns: ['type'],
      values: ['price', 'cost'],
    },
    meta: [
      { field: 'province', name: 'Province' },
      { field: 'city', name: 'City' },
      { field: 'type', name: 'Category' },
      { field: 'price', name: 'Price' },
      { field: 'cost', name: 'Cost' },
    ],
    data: [
      // ... your data
    ],
  };

  const onMounted = (spreadsheet: SpreadSheet) => {
    console.log('onMounted:', spreadsheet);
  };

  const onUpdate = (renderOptions: S2RenderOptions) => {
    console.log('onUpdate:', renderOptions);
    return renderOptions;
  };

  const onUpdateAfterRender = (renderOptions: S2RenderOptions) => {
    console.log('onUpdateAfterRender:', renderOptions);
  };

  return (
    <SheetComponent
      dataCfg={dataCfg}
      options={s2Options}
      onMounted={onMounted}
      onUpdate={onUpdate}
      onUpdateAfterRender={onUpdateAfterRender}
    />
  );
};
```

## Example 2: React TableSheet

Set `sheetType="table"` to render a flat table layout.

```tsx
import React from 'react';
import { S2DataConfig, type S2RenderOptions, type SpreadSheet } from '@antv/s2';
import { SheetComponent, SheetComponentOptions } from '@antv/s2-react';
import '@antv/s2-react/dist/s2-react.min.css';

const App: React.FC = () => {
  const s2DataConfig: S2DataConfig = {
    fields: {
      columns: ['province', 'city', 'type', 'price', 'cost'],
    },
    meta: [
      { field: 'province', name: 'Province' },
      { field: 'city', name: 'City' },
      { field: 'type', name: 'Category' },
      { field: 'price', name: 'Price' },
      { field: 'cost', name: 'Cost' },
    ],
    data: [
      // ... your data
    ],
  };

  const s2Options: SheetComponentOptions = {
    width: 600,
    height: 480,
  };

  const onMounted = (spreadsheet: SpreadSheet) => {
    console.log('onMounted:', spreadsheet);
  };

  return (
    <SheetComponent
      dataCfg={s2DataConfig}
      options={s2Options}
      sheetType="table"
      onMounted={onMounted}
    />
  );
};
```

## Example 3: React Editable TableSheet

Set `sheetType="editable"` to enable inline cell editing with frozen rows/columns support.

```tsx
import React from 'react';
import { S2DataConfig } from '@antv/s2';
import {
  SheetComponent,
  SheetComponentOptions,
  type SheetComponentsProps,
} from '@antv/s2-react';
import '@antv/s2-react/dist/s2-react.min.css';

const App: React.FC = () => {
  const s2DataConfig: S2DataConfig = {
    fields: {
      columns: ['province', 'city', 'type', 'price', 'cost'],
    },
    meta: [
      { field: 'province', name: 'Province' },
      { field: 'city', name: 'City' },
      { field: 'type', name: 'Category' },
      { field: 'price', name: 'Price' },
      { field: 'cost', name: 'Cost' },
    ],
    data: [
      // ... your data
    ],
  };

  const s2Options: SheetComponentOptions = {
    width: 480,
    height: 480,
    seriesNumber: {
      enable: true,
    },
    frozen: {
      rowCount: 1,
      colCount: 1,
      trailingRowCount: 1,
      trailingColCount: 1,
    },
  };

  const onDataCellEditStart: SheetComponentsProps['onDataCellEditStart'] = (
    meta,
    cell,
  ) => {
    console.log('onDataCellEditStart:', meta, cell);
  };

  const onDataCellEditEnd: SheetComponentsProps['onDataCellEditEnd'] = (
    meta,
    cell,
  ) => {
    console.log('onDataCellEditEnd:', meta, cell);
  };

  return (
    <SheetComponent
      dataCfg={s2DataConfig}
      options={s2Options}
      sheetType="editable"
      onDataCellEditStart={onDataCellEditStart}
      onDataCellEditEnd={onDataCellEditEnd}
    />
  );
};
```
