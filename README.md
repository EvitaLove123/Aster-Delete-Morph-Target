# Aster Delete Morph Target

A lightweight, mobile-friendly VRM morph-target cleanup tool for GitHub Pages.

## Features
- Load VRM 0.x and VRM 1.0 (GLB container).
- Preview the avatar in the browser.
- Browse and search morph targets by mesh.
- Select multiple targets and remove them.
- Update VRM expression morph-target bindings and export a cleaned .vrm.
- Original file is kept unchanged; processing happens locally in the browser.

## Deploy on GitHub Pages
1. Open **Settings → Pages**.
2. Under **Build and deployment**, choose **Deploy from a branch**.
3. Select branch **main**, folder **/(root)**, then Save.
4. Wait for the Pages deployment to finish.

## Notes
- The preview libraries are loaded from jsDelivr on first use, so an internet connection is required to load the app and its 3D dependencies.
- The model itself is not uploaded to a server.
- The tool edits the GLB JSON chunk and preserves the original binary chunks. Unused morph-target accessors may remain in the file, so file size may not shrink substantially.
- Please validate exported models in your target VRM application before replacing your original file.
- VRM animation tracks that animate morph-target weights are not remapped in this first version. Models with such animation tracks should be tested carefully.
