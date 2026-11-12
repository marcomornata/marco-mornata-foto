# Copilot Instructions for Marco Mornata Foto

## Project overview
This repository is a static photography portfolio website for Marco Mornata. The app is implemented as a plain HTML/CSS/JavaScript single-page gallery with no build tooling, framework, or package manager. The main entry point is `index.html`; image assets are stored in the `galleria*/` folders and the logo SVGs are in the repository root.

## Codebase conventions
- Keep changes small, surgical, and compatible with the existing single-page structure.
- Prefer editing `index.html` for layout, content, and behavior changes unless the change clearly belongs in a separate asset file.
- Preserve the current visual language: minimalist black/off-white palette, thin typography, subtle motion, and a premium editorial feel.
- Keep the Italian-language UI labels and gallery naming conventions consistent with the existing site.
- Do not introduce frameworks, bundlers, TypeScript, or package dependencies unless explicitly requested.

## UI and behavior expectations
- Maintain the existing hash-based navigation (`#0`, `#1-*`, `#2`, `#3`, `#4`, `#5`) and the fixed header layout.
- Preserve the home screen animation, overview gallery grid, tag-based filtering, and gallery detail views.
- Keep `contentGalleries` and related gallery IDs in sync when adding or renaming galleries.
- When adding new photos, follow the existing asset pattern (`galleriaN/fotoX.jpg`), and keep the image references consistent with the JavaScript gallery configuration.
- Keep accessibility in mind: use meaningful `alt` text and maintain keyboard-accessible button semantics.

## Styling rules
- Prefer CSS-based changes that match the current design system instead of redesigning the page.
- Respect the existing transitions, spacing, and mobile breakpoints already defined in `index.html`.
- Avoid changing the document structure or IDs used by the JavaScript without updating the corresponding JS logic.

## Validation
- This project does not have a build or test suite. Validate changes by serving the site locally and confirming the page loads without obvious JavaScript or asset errors.
- A minimal validation command is:
  - `python3 -m http.server 8000`
  - then visit `http://localhost:8000/` in a browser or use `curl` to fetch the page.
- When changing gallery content, verify that image paths still resolve correctly and that the filters and navigation still work as expected.

## Change scope
- Keep edits targeted to the exact feature being changed.
- Avoid unrelated cleanup or refactors.
- If you add or remove gallery entries, update both the gallery data and the UI labels so that the overall site remains coherent.
