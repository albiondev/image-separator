# Local Image Layer Separator — V6

GitHub Pages-ready prototype.

## iPhone/Safari upload

V6 deliberately uses one visible native `<input type="file">`. There is no JavaScript-triggered picker and no hidden duplicate picker.

After choosing an image, the status should immediately say `Selected ... — preparing image…`.

## Deploy

Replace `index.html` in the GitHub repository and commit. Keep GitHub Pages set to `main` and `/ (root)`.

Images are processed in the browser; the application does not upload image pixels to an application server.
