# Local Image Layer Separator — V8

GitHub Pages-ready browser prototype.

## iPhone / Safari upload

V8 adds an explicit **Use selected image** button. After choosing an image with Safari's native file picker, tap that button. The application reads `input.files[0]` directly and starts the existing image-analysis pipeline.

This provides a reliable fallback if iOS Safari does not fire the `change` event in the deployed page.

## Deploy

Replace `index.html` in the GitHub repository and commit. Keep GitHub Pages on `main` → `/ (root)`.

## Privacy

Image pixels are processed in the browser and are not sent to an application server.
