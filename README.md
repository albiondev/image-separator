# Local Image Layer Separator — V20

Deep pre-flight-checked build.

V20 fixes the scope issue found during the final deep check of V19. The processing-stage helper is explicitly attached to `window` as `window.setProcessingStage()` and all calls explicitly use `window.setProcessingStage()`.

Checks passed:
- each JavaScript block syntax-checked independently
- exactly one native file input
- all DOM references exist
- no `setStage()` references
- no conflicting `stage` variable
- explicit global processing-stage helper and calls
- Safari-sensitive analysis function termination
- delayed Transformers.js import
- BiRefNet Lite / RawImage pipeline wiring
- no obvious application-side image upload API
- malformed literal escape check

Replace `index.html` in the GitHub Pages repository and commit the change.
