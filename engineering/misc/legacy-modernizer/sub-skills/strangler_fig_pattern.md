---
name: strangler_fig_pattern
description: Use when executing strangler_fig_pattern protocols within the engineering sector.
---

# Strangler_Fig_Pattern: Execution Protocol

## ⚙️ Overview
This protocol defines the exact standards for implementing Strangler_Fig_Pattern. By following this strict operational pattern, the engine guarantees deterministic execution, high performance, and complete adherence to all architectural guardrails established by the system design.

# 🧶 Strangler Fig Pattern

Chiến thuật hiện đại hóa hệ thống cũ mà không cần đập đi xây lại hoàn toàn.

### 1. Identify (Xác định)
- Chọn một Module nhỏ nhất, ít rủi ro nhất trong hệ thống Legacy (Mage).

### 2. Wrap (Bọc)
- Tạo một Proxy/Gateway để điều hướng traffic.
- Traffic cho Module cũ vẫn đi vào hệ thống cũ.

### 3. Replace (Thay thế)
- Xây dựng Module mới trên công nghệ hiện đại.
- Điều hướng Proxy sang Module mới.

### 4. Remove (Gỡ bỏ)
- Sau khi Module mới hoạt động ổn định, gỡ bỏ code cũ tương ứng.
- Lặp lại cho đến khi toàn bộ hệ thống cũ được "siết chết" bởi hệ thống mới.
