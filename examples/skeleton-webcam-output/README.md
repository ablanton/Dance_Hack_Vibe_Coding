# Skeleton webcam → output

Records pose from your webcam and **outputs JSON** you can load in the [skeleton-avatar-threejs](../skeleton-avatar-threejs/) example.

## What it does

- Same live skeleton overlay as `skeleton-webcam`, plus:
- **Current frame data** – shows the 33 landmark arrays (world 3D in meters, and image 2D).
- **Record** – capture pose frames while you move.
- **Stop** – stop recording.
- **Download JSON** – save a `pose-recording.json` file. Use **Choose file** in the [Three.js avatar](../skeleton-avatar-threejs/) example to load it and replay your motion in 3D.
- **Stream to avatar** – check this, then open [avatar-viewer](../avatar-viewer/) (or [avatar-viewer-mixamo](../avatar-viewer-mixamo/) for a Mixamo FBX character) in another tab (same origin, e.g. same Live Server). The viewer shows only the 3D skeleton, driven live by this page’s pose data (no WebSockets; uses the browser’s BroadcastChannel).

## Run it

Use **Live Server** (right‑click `index.html` → Open with Live Server) or any local HTTP server. Webcam required.

## JSON format

The downloaded file has:

- `version`, `info`, `numLandmarks`, `connections` (same as MediaPipe pose connections).
- `fps` – nominal frame rate.
- `frames` – array of `{ "t": seconds, "world": [[x,y,z], ...] }` for each recorded frame. `world` is 33 points in meters (origin at hips), ready for 3D replay.
