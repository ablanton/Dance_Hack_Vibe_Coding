# Real-time skeleton → 3D avatar

**One page:** webcam pose drives the Three.js 3D skeleton **live**. No recording, no file—just you and the avatar in sync.

## What it does

- **Webcam** (small preview, top-right) runs MediaPipe Pose Landmarker.
- **3D avatar** (main view) is updated every frame from the same pose data.
- **Orbit** – drag to rotate the camera, scroll to zoom.

Same pipeline as [skeleton-webcam-output](../skeleton-webcam-output/) → [skeleton-avatar-threejs](../skeleton-avatar-threejs/), but in real time and all in one place.

## Run it

Use **Live Server** (right‑click `index.html` → Open with Live Server) or any local HTTP server. Webcam required.

## Pipeline

1. **skeleton-webcam** – Live pose only.
2. **skeleton-webcam-output** – Record pose, download JSON.
3. **skeleton-avatar-threejs** – Load JSON, replay in 3D.
4. **This example** – Webcam → 3D avatar in real time (no recording).
