---
version: 1.0.0-DRAFT
name: youtube-visuals
description: "High-CTR Engine: Generates viral thumbnails using 2026 visual psychology (0.5s Rule, Curiosity Gap)."
---

# 📺 YouTube Visuals: High-CTR Engine [DRAFT]

This skill engineers thumbnails designed to stop the scroll in under 500ms. It prioritizes psychological triggers over purely aesthetic choices.

## 🛡️ 1. The 2026 Design Pillars
1.  **The 0.5-Second Rule**: The design must answer "What is this?" instantly.
2.  **The Curiosity Gap**: Create a mystery that only the video title/content can solve. **RULE**: Never repeat the title text in the thumbnail.
3.  **2-3 Element Hierarchy**: Maximum of one subject, one hero object, and one text block. Clutter = Death.

## 🏗️ 2. Industrial Visual Protocol
- **Typography**: Bold, sans-serif (3-5 words max). High contrast (Outline/Shadow mandatory).
- **Color Theory**: Use complementary pairs (Orange/Blue, Yellow/Violet). Bright subjects on dark backgrounds.
- **Faces**: Authentic, tasteful expressions (Surprise, Focus, Disbelief). Avoid "YouTube Face" hyper-exaggeration.
- **Safe Zones**: Keep the bottom-right corner (150x50px) empty for the YouTube timestamp.

## 🧪 The "Squint Test" (Verification)
1.  **Action**: Shrink the design to 160px width.
2.  **Pass**: If the subject and text are still readable and the "story" is clear.
3.  **Fail**: If the design becomes a blurry mess. Simplify immediately.

## ⌨️ Commands (Draft)
| Command | Action |
| :--- | :--- |
| `/thumb-concept [title]` | Calls `youtube_visuals.py concept` to generate 3 viral hooks. |
| `/thumb-generate [concept]` | Triggers `generate_image` based on the chosen hook. |
| `/thumb-audit` | Runs the "Squint Test" and visual hierarchy audit. |
| `/thumb-evolve` | Analyzes previous thumbnail performance to refine the Design Pillars. |

---
*Status: DRAFT. Pattern: Validated (Industrial Recon).*
