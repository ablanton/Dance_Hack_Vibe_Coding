# Skeleton from webcam

Live skeletal pose from your webcam using **MediaPipe Pose Landmarker** (33 body landmarks in 2D and 3D).

## What it does

- Captures video from your camera
- Runs pose detection every frame and draws the skeleton overlay (bones + joints)
- Exposes both **image landmarks** (2D, used for drawing) and **world landmarks** (3D in meters) — you can hook `result.worldLandmarks[0]` into a 3D renderer (e.g. Three.js) for a 3D skeleton scene

## Run it

**Requires a webcam and a local server** (browser security blocks camera from `file://`).

**Easiest for workshops:** use **Live Server** in Cursor/VS Code: right‑click `index.html` → **Open with Live Server**. The page will open at `http://127.0.0.1:5500/...` (or similar). Allow camera access when prompted.

Other options:
- From this folder: `npx serve .` then open the URL shown.
- From repo root: `npx serve examples/skeleton-webcam` or `python3 -m http.server 8000` and open `http://localhost:8000/examples/skeleton-webcam/`.

No install step: the page loads MediaPipe from a CDN.

## Dependencies

- None locally. Uses:
  - [MediaPipe Tasks Vision](https://www.npmjs.com/package/@mediapipe/tasks-vision) (loaded from jsDelivr CDN)
  - Google-hosted `pose_landmarker_lite.task` model

## Next steps

- Use `result.worldLandmarks[0]` to drive a 3D skeleton in Three.js or another WebGL renderer.
- Map landmark positions to sound, visuals, or other creative outputs.
