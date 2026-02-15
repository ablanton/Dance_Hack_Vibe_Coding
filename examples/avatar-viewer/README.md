# Avatar viewer (live stream)

**Renders only the 3D avatar.** Receives pose data in real time from [skeleton-webcam-output](../skeleton-webcam-output/) via **BroadcastChannel** (browser tab-to-tab, no server).

## How to use

1. Serve both pages from the **same origin** (e.g. same Live Server: `http://127.0.0.1:5500`).
2. Open **skeleton-webcam-output** in one tab. Allow camera, then check **Stream to avatar**.
3. Open **avatar-viewer** in another tab (use “Open avatar viewer (new tab)” or open `examples/avatar-viewer/index.html`).
4. Move in front of the camera in the first tab; the second tab shows only the 3D skeleton, updated live.

No WebSockets or backend: the browser’s BroadcastChannel API sends the same JSON-style pose data from the webcam tab to the viewer tab.

## Run it

Use **Live Server** so both examples share the same origin. If you open one from `file://` and the other from localhost, they won’t see each other.
