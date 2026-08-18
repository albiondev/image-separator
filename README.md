# Local Image Layer Separator — V11

V11 adds explicit startup diagnostics. The upload bootstrap is dependency-free and catches browser JavaScript errors and rejected promises. The application engine is initialised separately.

If the application fails before registering its analysis function, the status area now reports the JavaScript startup error instead of silently remaining on “Waiting for image”.

Deploy by replacing `index.html` in the GitHub Pages repository and committing the change.
