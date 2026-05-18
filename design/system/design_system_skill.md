# Design_System_Skill: Execution Protocol

## ⚙️ Overview
This protocol defines the exact standards for implementing Design_System_Skill. By following this strict operational pattern, the engine guarantees deterministic execution, high performance, and complete adherence to all architectural guardrails established by the system design.

---
version: 1.0.0
name: design-system
description: "Industrial Design Language: Defines the tokens, typography, and visual rules for premium web development."
---

# 🎨 Master Design System: "Antigravity Premium"

This skill governs the visual identity of all web applications produced by the engine.

## 🌈 1. Color Palettes
### A. "Obsidian Gold" (Luxury/Jewelry)
- **Primary**: `hsl(45, 100%, 50%)` (Gold)
- **Background**: `hsl(0, 0%, 5%)` (Obsidian)
- **Surface**: `hsla(0, 0%, 15%, 0.7)` (Glass)
- **Accent**: `hsl(160, 100%, 15%)` (Emerald)

### B. "Arctic Neon" (Tech/SaaS)
- **Primary**: `hsl(210, 100%, 50%)` (Electric Blue)
- **Background**: `hsl(230, 20%, 10%)` (Deep Space)
- **Surface**: `hsla(210, 20%, 20%, 0.5)` (Frosted Glass)

## 🖋️ 2. Typography
- **Headings**: `Outfit` or `Playfair Display` (Serif)
- **Body**: `Inter` or `Roboto`
- **Monospace**: `JetBrains Mono`

## 💎 3. Visual Rules
- **Radius**: `12px` (Standard Card), `999px` (Pill).
- **Glassmorphism**: `backdrop-filter: blur(12px) saturate(180%)`.
- **Shadows**: `0 10px 30px -5px rgba(0,0,0,0.5)`.
- **Transitions**: `0.3s cubic-bezier(0.4, 0, 0.2, 1)`.

## 🏗️ 4. Global Variables (CSS)
```css
:root {
  --bg: #0a0a0a;
  --surface: rgba(255, 255, 255, 0.05);
  --primary: #f59e0b;
  --text-main: #ffffff;
  --text-dim: #a1a1aa;
  --blur: blur(12px);
  --radius: 12px;
}
```

---
*Status: INITIALIZED. Usage: Mandatory for all UI tasks.*
