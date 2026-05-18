---
name: zero_downtime_strategy
description: Use when executing zero_downtime_strategy protocols within the engineering sector.
---

# Zero_Downtime_Strategy: Execution Protocol

## ⚙️ Overview
This protocol defines the exact standards for implementing Zero_Downtime_Strategy. By following this strict operational pattern, the engine guarantees deterministic execution, high performance, and complete adherence to all architectural guardrails established by the system design.

# 🗄️ Zero-Downtime Migration Strategy

Quy trình nâng cấp Database không làm gián đoạn người dùng.

### Bước 1: Expand
- Thêm cột mới (cho phép NULL).
- Ứng dụng hỗ trợ cả cột cũ và cột mới.

### Bước 2: Migrate
- Chạy script ngầm để copy dữ liệu từ cột cũ sang cột mới.
- Cập nhật ứng dụng để ghi dữ liệu vào CẢ HAI cột.

### Bước 3: Contract
- Thay đổi ứng dụng để chỉ đọc từ cột mới.
- Dừng việc ghi vào cột cũ.

### Bước 4: Delete
- Xóa bỏ cột cũ sau khi xác nhận hệ thống ổn định 100%.

> **Lưu ý**: Tuyệt đối không thực hiện RENAME cột trực tiếp trên DB đang chạy tải cao.
