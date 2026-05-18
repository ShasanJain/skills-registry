---
version: 1.0.0
name: janitor
description: "Industrial Maintenance: Cleans temporary production assets and transient files to maintain system health."
---

# 🧹 Janitor: Industrial Maintenance

This skill manages the cleanup of the production pipeline, ensuring that temporary images, audio segments, and renders do not consume unnecessary disk space.

## 🛡️ 1. Cleanup Protocol
- **Target 1**: `video/public/assets/scenes/*.png` (excluding templates).
- **Target 2**: `video/public/assets/audio/*.mp3`.
- **Target 3**: Root `output.mp4` and `video_manifest.json`.
- **Target 4**: `scratch/` directory transient scripts.

## 🏗️ 2. Industrial SOP
1.  **Safety**: Verify that the latest render has been backed up or delivered to the user.
2.  **Execution**: Run `janitor.py` to purge transient data.
3.  **Verification**: Confirm directory sizes are reset.

## ⌨️ Commands
| Command | Action |
| :--- | :--- |
| `/clean` | Runs the full industrial cleanup protocol. |

---
*Status: INITIALIZED. Pattern: Hygiene/Optimization.*
