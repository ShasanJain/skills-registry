---
version: 1.0.0
name: video-depth
description: "3D Parallax Architect: Generates depth maps for static images to enable local 3D motion."
---

# 📐 Video Depth: 3D Parallax Architect

This skill transforms 2D static images into 3D depth maps, allowing for realistic camera movement (dolly zoom, parallax) without needing high-VRAM video generation.

## 🛡️ 1. Technical Specs
- **Model**: MiDaS (Small/v2.1) - Optimized for 4GB VRAM.
- **Output**: Greyscale depth map (PNG).
- **Integration**: Injected into Remotion `ClipEngine` for 3D displacement.

## 🏗️ 2. Industrial Protocol
1.  **Input**: High-contrast 2D image.
2.  **Process**: Run `video_depth.py` to extract Z-buffer data.
3.  **Assembly**: Map depth data to Remotion `displacementMap`.

## ⌨️ Commands
| Command | Action |
| :--- | :--- |
| `/video-depth [image_path]` | Generates a depth map for the target image. |

---
*Status: INITIALIZING. Pattern: Local/Efficient.*
