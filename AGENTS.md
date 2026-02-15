# Agent guidance – creative applications

Use this file to orient AI agents working on **Dance Hack** and other creative/vibe-coding projects in this repo.

## Project context

- **Focus:** Creative applications, vibe coding, and performance-oriented code (e.g., dance, music, visuals, live interaction).
- **Goal:** Build small, runnable experiments and demos that prioritize expressiveness and immediacy over production polish.

## Structure

- **`/examples`** – Self-contained creative app examples. Each example should run on its own and have a short README or comment describing what it does and how to run it.
- **Root** – Shared docs (README, this file), and optional shared utilities if they emerge from examples.

## Creating a new creative application

When adding a new example or creative app:

1. **Scope** – Prefer one clear idea per example (e.g., one visualization, one controller, one generative pattern).
2. **Run instructions** – Include in the example folder:
   - How to install dependencies (if any).
   - How to run (e.g., `npm start`, `python app.py`, open `index.html`).
3. **Dependencies** – Prefer minimal, well-known tools. Call out any required hardware (e.g., webcam, MIDI) in the example’s README or top-of-file comments.
4. **Portability** – Favor technologies that run in the browser or with a single runtime (e.g., Node, Python) so others can try the example quickly.

## Conventions

- **Language/tooling** – No single stack is required; choose what fits the example (e.g., p5.js, Three.js, vanilla JS, Python, Max/MSP, etc.).
- **Documentation** – Each example should have at least:
  - A one-line description.
  - How to run it.
  - Any setup (env vars, keys, hardware) if needed.
- **Naming** – Use short, descriptive names for example folders (e.g., `beat-viz`, `motion-mirror`, `generative-grid`).

## What “creative application” means here

- Code that drives or responds to **performance** (dance, music, spoken word, etc.).
- **Generative** or **reactive** visuals/sound.
- **Live interaction** (sensors, camera, MIDI, touch, keys).
- **Vibe coding** – fast iteration, playful exploration, and clear cause-and-effect over strict architecture.

When in doubt, favor something that is easy to run, easy to tweak, and fun to experience.
