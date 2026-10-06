# GridScale

Offline HTML/SVG generator for grid-locked dot patterns with controlled dynamic scale variation.

## Run
Open `index.html` in any modern browser. No server, npm, or internet connection is required.

## Core behavior
- Dot positions are mathematically locked to a rectangular grid.
- Scale is randomized from a deterministic seed.
- Spatially correlated value noise prevents the pattern from looking like unstructured white noise.
- Density can hide/reveal dots without moving the remaining dots.
- Export standards-compliant SVG or 2× PNG.
- **Copy SVG** writes an actual `image/svg+xml` clipboard payload when the browser supports it, so `Cmd/Ctrl + V` into Figma pastes vector paths/shapes rather than a raster image.
- SVG output includes a single valid SVG namespace and XML declaration, avoiding the duplicate-`xmlns` bug that caused Illustrator's “This SVG is Invalid” warning.
- Buttons have hover/active/focus states and success feedback.
- Change seed and press Randomize for a new pattern.

## Figma
Use **Copy SVG → paste directly into Figma**. The preferred Clipboard API writes both `image/svg+xml` and plain-text SVG fallbacks. If the browser blocks rich clipboard access, use **Export SVG** and import the file into Figma.
