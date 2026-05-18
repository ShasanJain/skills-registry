# Visually: Execution Protocol

## ⚙️ Overview
This protocol defines the exact standards for implementing Visually. By following this strict operational pattern, the engine guarantees deterministic execution, high performance, and complete adherence to all architectural guardrails established by the system design.

---
description: Visualize complex logic, architecture, and mindmaps.
---

## 👁️ Quy trình Trực quan hóa Tri thức

Chuyển đổi code và logic trừu tượng thành sơ đồ dễ hiểu (Mermaid / SVG).

### 1. Phân tích Mã nguồn
- Chuyên gia: `code-archaeologist`.
- Quét dự án để tìm ra các module cốt lõi và mối liên hệ qua lại.

### 2. Vẽ Sơ đồ (Render)
- Tạo sơ đồ Flowchart, Sequence hoặc Class Diagram.
- Xuất định dạng SVG hoặc nhúng trực tiếp vào README.

### 3. Giải thích Kỹ thuật
- Phụ tá: `debugger` hoặc `documentation-writer`.
- Đưa ra bối cảnh (Context) cho từng khối logic trong sơ đồ.

// turbo
`npx mmd-render flowchart.mmd`
