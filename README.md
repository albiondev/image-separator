# Local Image Layer Separator — V10

## Why V10 is different

The previous full app had a JavaScript startup failure. The native Safari picker still appeared, but the application script could fail before its event handlers were registered. V10 separates the upload bootstrap from the AI application.

The first script is a tiny classic browser script with no external dependencies. It:

1. Receives the selected file.
2. Creates a local object URL.
3. Decodes and previews the image.
4. Only then starts the AI application.

The AI library is dynamically imported after the image has successfully loaded.

The JavaScript was also syntax-checked before packaging.

## Deploy

Replace `index.html` in the GitHub repository and commit it. Keep GitHub Pages on `main` → `/ (root)`.

## Privacy

Image pixels are processed in the browser and are not sent to an application server.
