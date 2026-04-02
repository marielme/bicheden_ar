# bichedenAR

A small Web AR demo using MindAR (image tracking) with A-Frame.

## Quick start

1. Serve the project from the project root (do not open the file directly).
   - Using Node: `npx serve`
   - Or with Python: `python -m http.server 8000`
2. Open the site at `http://localhost:3000` (or the port your server reports).
3. Allow camera access when prompted and point your camera at the prepared image target.

## What this repo contains

- `index.html` — main app (A-Frame + MindAR) that loads the image tracker and content.
- `assets/` — images, models, and target files used by the scene.
- `targets.mind` — project image target file (generated for MindAR).

## Image targets (MindAR)

This project uses MindAR for image tracking. 

1. Read the MindAR docs for image tracking and target generation: https://hiukim.github.io/mind-ar-js-doc/
2. Generate a MindAR image target file (`.mind`) using the MindAR image-target generator (follow the docs). The generator converts your source image into a `.mind` file.
3. Place the generated `.mind` file in `assets/` (or keep using the existing `targets.mind` at the project root) and ensure `index.html` references the correct path to that file.

## Adding 3D content

1. Add a `.gltf`/`.glb` model to `assets/models/`.
2. Reference it inside the MindAR scene in `index.html` with an appropriate entity (for example an `<a-entity gltf-model="assets/models/yourmodel.gltf">`).

## Notes

- Serve over `localhost` or HTTPS to enable camera access.
- MindAR target files are `.mind` .
- Keep models optimized for mobile browsers.


