# Aster GLB Model Delete

A mobile-friendly, browser-local GLB 2.0 cleanup tool. **GLB only** — VRM files are not supported.

## Features
- Import and export binary `.glb` files.
- 3D preview (automatically skipped for larger files to reduce mobile memory pressure).
- Search and multi-select Morph Targets.
- Remove selected Morph Targets.
- Search and multi-select Meshes.
- Remove selected Meshes and remap node mesh references.
- Reset to the original file.
- All model processing happens locally in the browser; files are not uploaded.

## GitHub Pages
1. Open **Settings → Pages**.
2. Choose **Deploy from a branch**.
3. Select branch **main** and folder **/(root)**.
4. Save and wait for deployment.

## Important limitations
- This version accepts GLB 2.0 binary files only. It does not accept VRM or separate .gltf + .bin files.
- Removing targets or meshes updates the GLB JSON structure, but unused binary buffer data and accessors are not compacted. The exported file may therefore not become much smaller.
- Mesh removal removes mesh references from nodes; it does not perform advanced skeleton/animation cleanup or delete unused materials and textures.
- Large-file preview is skipped to reduce memory use on Android. Editing still runs in the browser, but very large models may exceed available device memory.
- Keep the original file and validate exported GLB in a compatible viewer before using it.
