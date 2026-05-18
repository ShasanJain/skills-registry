---
version: 1.0.0
name: video-visuals
description: "Kinetic Prompt Engine: Generates highly detailed scene prompts for AI video generation."
---

# 🎬 Video Visuals: Kinetic Prompt Engine

This skill engineers prompts that describe movement, lighting, and cinematic camera work for AI video models (Sora, Runway, Pika).

## 🛡️ 1. The Visual Pillars
1.  **Camera Movement**: Define pans, tilts, zooms, or "dolly shots."
2.  **Kinetic Motion**: Describe the speed and direction of subjects (e.g., "rapidly sprinting," "slow-motion descent").
3.  **Cinematic Lighting**: Use terms like "Golden Hour," "Rim Lighting," "Volumetric Fog."
4.  **Temporal Consistency**: Ensure prompts across scenes maintain character and environment details.

## 🏗️ 2. Industrial Visual Protocol
- **Subject**: Who/What is in the scene.
- **Action**: What is happening (Verb-heavy).
- **Environment**: Where is it happening (Atmospheric).
- **Camera**: How is it being filmed (Technique).

## ⌨️ Commands
| Command | Action |
| :--- | :--- |
| `/video-scene [story]` | Calls `video_visuals.py` to generate 3 detailed scene prompts. |

---
*Status: STABLE. Pattern: Industrial.*
