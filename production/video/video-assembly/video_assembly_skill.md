---
version: 1.0.0
name: video-assembly
description: "Production Forge: Orchestrates the final video build using Remotion and React."
---

# 🛠️ Video Assembly: Production Forge

This skill assembles all assets (Video, Audio, Captions) into a final render-ready project using Remotion.

## 🛡️ 1. The Assembly Pillars
1.  **Project Scaffolding**: Create a clean Remotion project structure.
2.  **Asset Linking**: Map file paths to Remotion `<Video>`, `<Audio>`, and `<Sequence>` components.
3.  **Composition Logic**: Handle frame-rate, dimensions, and total duration calculations.
4.  **Local Rendering**: Orchestrate the final `.mp4` build using FFMPEG and Remotion CLI.

## 🏗️ 2. Industrial Assembly Protocol
- **Folder Structure**: `video/src`, `video/public/assets`.
- **Manifest**: `video_manifest.json` containing timing and file references.
- **Render**: Use `python execution/video_assembly.py render` to produce `output.mp4`.

## ⌨️ Commands
| Command | Action |
| :--- | :--- |
| `/video-build [manifest]` | Calls `video_assembly.py` to scaffold the project. |
| `/video-render` | Calls `video_assembly.py` to generate the final .mp4 file. |


---
*Status: STABLE. Pattern: Industrial.*
