# Local Image Layer Separator — V7

GitHub Pages-ready prototype.

## iPhone / Safari upload

The upload path is based on a minimal Safari diagnostic that was verified to receive and preview a selected image. The app uses one native `<input type="file">` and the same `change`/FileReader-compatible browser flow before handing the file to the layer-separator pipeline.

## Features

- Browser-side AI foreground/background segmentation
- Local OCR
- Estimated typography, text-background, decoration and background layers
- Adjustable edge softness
- 1× / 2× / 4× / custom output resolution
- Transparent PNG export
- No application server for image processing

## Deploy

Replace the repository's `index.html` with this file and commit it. Keep GitHub Pages on `main` → `/ (root)`.

## Privacy

Image pixels are processed in the browser and are not sent to an application server. Libraries and model files are downloaded from their CDNs/model hosting.
