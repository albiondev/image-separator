# Local Image Layer Separator

GitHub Pages-ready browser prototype for local image layer separation.

## Mobile Safari

The upload control uses a native HTML file input associated with a `<label>`, rather than programmatically calling `.click()` on a hidden input. This is intentionally more compatible with iPhone/iPad Safari.

When prompted, choose **Photo Library**, **Take Photo or Video**, or **Choose File** as appropriate.

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

The uploaded image is converted to a Transformers.js `RawImage` in-browser before inference.

## GitHub Pages

Upload `index.html` to the repository root, then use:

**Settings → Pages → Deploy from a branch → main → / (root)**

Commit changes and wait for the Pages deployment.

## Privacy

The app does not send the user's image to an application server. Libraries and model files are downloaded from their respective CDNs/model hosting.

## Licence note

Review all third-party dependency and model licences before commercial redistribution.
