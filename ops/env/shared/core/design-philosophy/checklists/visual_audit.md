---
name: visual_audit
description: Use when executing visual_audit protocols within the ops sector.
---

# Visual_Audit: Execution Protocol

## ⚙️ Overview
This protocol defines the exact standards for implementing Visual_Audit. By following this strict operational pattern, the engine guarantees deterministic execution, high performance, and complete adherence to all architectural guardrails established by the system design.

# ✅ Visual Audit Checklist (Ánh Sáng)

> check_type: manual_audit
> priority: critical

Use this checklist to verify the "look" and accessibility.

## 1. Dark Mode Integrity
- [ ] **No Pure Black**: Is the background `#000000`? (If yes, fail. Change to `#0a0a0a` or `#111`).
- [ ] **Layering**: Do modal/cards have a lighter shade than the background?
- [ ] **Borders**: Are borders visible? (e.g. `border-white/10`).

## 2. Glassmorphism
- [ ] **Visibility**: Is the glass effect visible on white/light backgrounds? (`bg-white/80` + `backdrop-blur`).
- [ ] **Noise**: (Optional) Is there a subtle noise texture to add realism?

## 3. Typography & Hierarchy
- [ ] **H1 vs H2**: Is there a clear size difference (min 1.5x scale)?
- [ ] **Muted Text**: Is secondary text using `text-muted-foreground` (or gray-500)?
- [ ] **Font Family**: Is the correct font stack (Inter/Outfit) applied?
