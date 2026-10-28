# HomeTour AI — MVP

A browser-based starter prototype for exploring a sample home in real-time 3D using Three.js.

## Features in this starter

- Upload a floor-plan file as a reference (JPG/PNG preview; PDF selection only)
- Change sample house width, depth, ceiling height and wall thickness
- Generate an illustrative 3D sample layout
- Switch among three material palettes
- Orbit overview and first-person WASD/mouse navigation
- Responsive interface

## Deploy to GitHub Pages

This repository includes a GitHub Actions workflow at `.github/workflows/pages.yml`.

1. Create a GitHub repository named `hometour-ai`.
2. Upload these files to the repository root, or push this folder using Git.
3. In GitHub, open **Settings → Pages**.
4. Under **Build and deployment**, select **GitHub Actions** as the source.
5. Push to the `main` branch or run the workflow from **Actions**.
6. When the workflow completes, GitHub will show the deployed URL under **Settings → Pages**.

The website is static and does not require a Node build step. Three.js is loaded from a CDN, so visitors need internet access.

## Run locally

With Python 3 installed, run this from the repository folder:

```bash
python3 -m http.server 8000
```

Open `http://localhost:8000`.

## Important limitations

This is a starter UI/3D prototype, not yet an AI floor-plan converter. The uploaded drawing is not parsed into model geometry. The rooms and furniture are illustrative; door openings, accurate window placement, robust collision detection, project saving, multi-floor support and photorealistic rendering are not implemented. Do not use generated geometry for construction or measurement.

## Next engineering steps

1. Build an editable 2D plan editor and scale calibration.
2. Add AI-assisted room/wall/dimension extraction with user verification.
3. Generate walls with explicit door and window openings.
4. Improve first-person collision and room navigation.
5. Add photorealistic materials, lighting and asset library.
6. Add authentication, private file storage, project persistence and processing jobs.

**Product principle:** never present an inferred measurement as verified. Flag ambiguous geometry and require user confirmation before generating the final model.
