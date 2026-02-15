# Avatar viewer (Mixamo FBX)

Same as [avatar-viewer](../avatar-viewer/) but uses a **Mixamo rigged character** (FBX) instead of the procedural body. The character is positioned from the pose stream (hip center); full limb retargeting from 33 landmarks can be added on top.

## Setup

1. **Place your Mixamo FBX** in one of these locations (so the page can load it):
   - This folder: `examples/avatar-viewer-mixamo/Ch36_nonPBR.fbx`
   - Or repo root: `DanceHack/Ch36_nonPBR.fbx`

2. Serve from the **same origin** (e.g. Live Server from repo root). Open [skeleton-webcam-output](../skeleton-webcam-output/), check **Stream to avatar**, then open this page (or use the viewer link from that page and change the path to `avatar-viewer-mixamo`).

## FBX vs GLB

- **FBX** works and is what Mixamo gives you. It can be large (ASCII FBX is verbose).
- **GLB** is often better for the web: one file, smaller, and Three.js’s GLTFLoader handles it well. To use GLB instead:
  1. In Mixamo, if you have a “Download” option that includes glTF/GLB, use that, or
  2. Convert FBX → GLB (e.g. in [Blender](https://www.blender.org/) or an online converter), then
  3. In this example we’d switch to `GLTFLoader` and load the `.glb` file instead of the FBX.

If you add a GLB, we can change the example to load `Ch36_nonPBR.glb` (or your filename) instead.

## Current behavior

- Loads the first FBX it finds from the paths above.
- Rotates the model 180° to match our pose space.
- Each frame: sets the **model position** to the hip center (midpoint of left/right hip landmarks) from the stream.
- Limb bones are not yet driven from the 33 landmarks; that would require mapping Mixamo bone names to landmark pairs and setting bone quaternions (doable as a next step).
