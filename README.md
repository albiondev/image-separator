# Local Image Layer Separator — V9

GitHub Pages-ready browser prototype.

## Important iPhone/Safari fix

The previous versions imported Transformers.js at page startup. If Safari failed to load that ES module, the entire application script stopped before the file-picker handlers were installed. That explains why the native picker could work in the diagnostic page but the full app remained stuck on “Waiting for image”.

V9 changes the architecture:

1. The page starts with no AI dependency import.
2. The native file input is available immediately.
3. Selecting the file reaches the application.
4. Only then does the page dynamically import Transformers.js.
5. Any model/library loading error is shown in the status box.

This isolates upload from AI startup.

## Deploy

Replace the repository `index.html` with this file and commit. Keep GitHub Pages on `main` → `/ (root)`.

## Privacy

Image pixels are processed in the browser. The application does not upload them to an application server.
