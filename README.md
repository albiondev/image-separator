# Local Image Layer Separator

GitHub Pages-ready browser prototype for local image layer separation.

## Features

- Browser-side AI foreground/background segmentation
- Local OCR
- Estimated typography, text-background, decoration and background layers
- Adjustable edge softness
- 1× / 2× / 4× / custom output resolution
- Transparent PNG export
- No application server for image processing

## Current AI stack

- Transformers.js
- onnx-community/BiRefNet_lite-ONNX for foreground segmentation
- Tesseract.js for OCR

The image is converted to a Transformers.js `RawImage` in-browser before inference. This avoids passing an unsupported `HTMLImageElement` object to the pipeline.

## GitHub Pages

Upload `index.html` to the repository root, then use:

**Settings → Pages → Deploy from a branch → main → / (root)**

Commit changes and wait for the Pages deployment to finish.

## Privacy

The app does not send the user's image to an application server. Libraries and model files are downloaded from their respective CDNs/model hosting.

## Licence note

BiRefNet Lite ONNX is published under the MIT licence, but review all third-party dependency/model licences before commercial redistribution.
