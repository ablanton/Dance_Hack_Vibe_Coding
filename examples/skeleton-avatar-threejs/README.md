# 3D skeleton avatar (Three.js)

Load a **pose recording JSON** (from [skeleton-webcam-output](../skeleton-webcam-output/)) and replay it as a **3D skeleton** in the browser.

## What it does

- **Load pose JSON** – Use “Load pose JSON” and choose a `pose-recording.json` file you downloaded from the output example.
- **Play / Pause** – Replay the recorded motion. The avatar is a 3D stick figure (joints + bones) driven by the 33 world landmarks.
- **Orbit** – Drag to rotate the camera, scroll to zoom.

The 3D figure uses the same landmark layout as MediaPipe (33 points, same connections). You can replace the simple sticks and spheres with a skinned GLB character and map these positions to your rig for a full-body avatar.

## Run it

Use **Live Server** (right‑click `index.html` → Open with Live Server) or any local HTTP server. No webcam needed; it only needs a JSON file.

## Pipeline

1. **skeleton-webcam** – See live pose from webcam.
2. **skeleton-webcam-output** – Record pose and download JSON.
3. **This example** – Load JSON and view 3D skeleton replay.

## JSON format expected

The file must contain an array of frames, each with a `world` array of 33 `[x, y, z]` points (meters). The output example produces this format.
