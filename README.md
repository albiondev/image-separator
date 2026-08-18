# Local Image Layer Separator — Final Pre-flight Build

This package has been pre-flight checked before release:
- each JavaScript block syntax-checked independently
- exactly one native file input
- all referenced DOM IDs exist
- Safari-sensitive analysis-function assignment explicitly terminated
- AI library import delayed until after image selection
- BiRefNet Lite model referenced
- no obvious application-side image upload endpoint
- processing-stage indicator included

Replace `index.html` in the GitHub Pages repository and commit the change. Keep Pages on `main` → `/ (root)`.

Images are processed in the browser. External library/model assets are downloaded from their CDNs/model hosting.
