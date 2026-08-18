# Local Image Layer Separator

A browser-based prototype for separating a flattened image into estimated layers:

- Typography
- Text background
- Image / decoration
- Whole-image background
- AI foreground

## Privacy

Images are processed in the browser. The prototype does not upload image pixels to an application server.

The app currently loads its JavaScript libraries and AI model from CDNs on first use:

- Transformers.js
- BRIA RMBG-1.4
- Tesseract.js

The BRIA RMBG-1.4 model has licence restrictions; review its model card before commercial distribution.

## Run locally

Open `index.html` in a modern browser, or serve the folder with a local static server.

## Deploy with GitHub Pages

1. Create a new GitHub repository.
2. Upload `index.html` and this `README.md`.
3. In GitHub, open **Settings → Pages**.
4. Under **Build and deployment**, choose **Deploy from a branch**.
5. Select the `main` branch and `/ (root)`.
6. Save.
7. GitHub will provide the Pages URL.

## Notes

This is an experimental V1. The layer decomposition is inferred from a flattened image, so it is not equivalent to recovering original Photoshop/Illustrator layers.

The next major improvement would be a dedicated local super-resolution / matting pipeline for better reconstruction of typography, fine artwork, shadows and glows.
