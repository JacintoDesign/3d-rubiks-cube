# Cube Lab

A responsive, vanilla HTML/CSS/JavaScript Rubik's Cube playground powered by Three.js. No build step is needed.

## Run

```sh
python3 -m http.server 5173
```

Open http://localhost:5173. Internet access is needed for the pinned Three.js CDN modules and Google Fonts.

## Controls

- Drag a cubie to turn its layer; drag empty space to orbit.
- Scroll or pinch to zoom. Right-drag or use two fingers to pan.
- Random scramble animates a randomized sequence; Solve reverses recorded turns, including manual moves. It is a history-based solver, not a shortest-path solver for imported states.
- Reset cancels playback and restores the solved cube and camera, retaining appearance settings.
- Changing grid size starts a new solved cube. Other appearance controls preserve its state.
- The camera buttons restore the view and toggle auto orbit.

Supports 2–6 layers, live surface and lighting settings, procedural carbon-fiber and brushed-metal textures, rounded geometry, and adjustable stickers. Only visible shell cubies are created. Geometry and materials are shared; layer animation uses temporary transform groups and exact half-integer grid coordinates to prevent accumulated position drift.

Files: `index.html` (UI), `style.css` (responsive styling), `app.js` (scene, state, interaction and animation).
