# Local Image Layer Separator — V12

V12 fixes the JavaScript startup error reported by Safari.

## Root cause

The previous version assigned:

`window.startLayerAnalysis = async function(file) { ... }`

and immediately followed it with an array expression. Because the assignment did not have a terminating semicolon, Safari parsed the array as a property access on the function expression, producing:

`undefined is not an object (evaluating 'async function(file){...} ["dragover"...')`

V12 explicitly terminates that assignment.

## Deploy

Replace `index.html` in the GitHub repository and commit the change. Keep GitHub Pages on `main` → `/ (root)`.

## Privacy

Images are processed in the browser; they are not uploaded to an application server.
