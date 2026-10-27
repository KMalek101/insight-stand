# INSIGHT STAND

An interactive Three.js particle experience created for **Insight Research Club**.

> "where curiosity meets clarity"

The experience uses MediaPipe hand tracking to transform a 3D particle cloud into different formations, including the Insight Research Club logo.

## Requirements

- A modern browser such as Chrome or Firefox
- A webcam
- Python 3
- `index.html` and `logo.png` in the same folder

## Run locally

Do not open `index.html` directly with `file://`. The logo pixel sampler and camera features require HTTP.

1. Open PowerShell in this folder.
2. Start a local web server:

   ```powershell
   python -m http.server 8000
   ```

3. Open this address in your browser:

   ```text
   http://127.0.0.1:8000/index.html
   ```

4. Allow camera access when prompted.

## Gestures

- Fist — Sphere
- Open hand — Scatter
- Point — Vortex
- Swipe — Push
- Thumb up — Insight Research Club logo

When no hand is detected, the logo returns to the idle state.

## Troubleshooting

- If the logo does not appear, confirm that `logo.png` is beside `index.html`.
- If the console reports a canvas security error, make sure the page was opened through `http://127.0.0.1:8000`, not `file://`.
- If the camera does not start, close other tabs using the webcam, allow camera permission, and reload the page.
- If the animation is slow, enable browser hardware acceleration and close other WebGL-heavy tabs.

## Project structure

```text
index.html  # application, styles, shaders, particle physics, and gesture handling
logo.png    # logo source image used for particle sampling
```
