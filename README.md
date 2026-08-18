# Local Image Layer Separator

A browser-based prototype for separating a flattened image into estimated layers.

## Current features

- Local browser-side image processing
- AI foreground/background segmentation using BiRefNet Lite
- Local OCR with Tesseract.js
- Estimated typography layer
- Estimated text-background layer
- Estimated decoration/foreground layer
- Whole-image background layer
- Adjustable edge softness
- 1× / 2× / 4× output scaling
- Custom output dimensions
- Aspect-ratio preservation
- High-quality transparent PNG export

## Privacy

The application does not upload the user's image to an application server. Image inference happens in the browser.

On first use, browser JavaScript libraries and AI model files are downloaded from CDNs/model hosting. Those downloads are separate from the image data.

## Deployment with GitHub Pages

1. Create or open a GitHub repository.
2. Upload `index.html` to the repository root.
3. Commit the change.
4. Open **Settings → Pages**.
5. Under **Build and deployment**, select **Deploy from a branch**.
6. Select the `main` branch and `/ (root)`.
7. Save.
8. GitHub will provide the public Pages URL.

## Important

This is an experimental V1. Layer separation is inferred from a flattened image; it cannot recover the exact original design layers.

The current segmentation model is `onnx-community/BiRefNet_lite-ONNX`. Review its model card and licence before commercial redistribution.

The next development stage should improve text extraction, alpha matting, shadow/glow preservation and dedicated super-resolution/reconstruction.
