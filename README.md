# ASCII-ART-CONVERTER
This HTML file is a complete, single-page **“ASCII Art Studio / ASCII Art Converter”** web app that lets you upload an image and convert it into different kinds of text/character art, entirely in the browser.

Source: `ascii_art_converter.html` (commit `a593c23b...`) from `Shubh-153/ASCII-ART-CONVERTER`.

## What it contains

### 1) UI / Layout (HTML)
- A centered app with three main panels inside a responsive grid:
  - **Input panel**: drag-and-drop / click-to-upload image area with a preview.
  - **Mode Guide panel**: description of the selected conversion mode, quick tips, and live “stats”.
  - **Output panel** (hidden until conversion): shows the generated text art in a `<pre>`, plus toolbar buttons.

### 2) Styling (CSS)
- A dark, neon-themed UI with an animated grid background.
- “Terminal-like” panels (header dots like macOS windows), mono font for outputs, gradients for headings/buttons.
- Output color changes by mode (binary/blocks/braille/emoji/matrix) and supports selecting a theme color via swatches.

### 3) Features & Controls
- **Modes (tabs):**
  - `ascii` (classic brightness-to-character mapping)
  - `binary` (0/1 threshold)
  - `blocks` (Unicode block shading characters)
  - `braille` (high-resolution Braille Unicode based on 2×4 pixel blocks)
  - `matrix` (random katakana/latin “Matrix” characters with glow)
  - `emoji` (color-matching emoji mosaic)
- **Character set selector** for ASCII-like modes (standard/dense/simple/minimal/letters/numbers).
- Sliders for:
  - **Resolution** (output columns; affects rows by aspect ratio)
  - **Contrast** (applied via canvas context filter)
  - **Brightness** (applied via canvas context filter)
- Checkboxes:
  - **Invert colors**
  - **Colored output (ANSI-style)** (present in UI; the code mainly uses CSS color on the `<pre>` rather than emitting ANSI escape codes)
  - **Edge detection mode** (Sobel-like gradient + angle-to-`-|/\` characters)

### 4) Image processing (JavaScript)
- Uses a hidden `<canvas>` to:
  - resize the uploaded image to a computed grid size,
  - apply contrast/brightness via `ctx.filter`,
  - read pixel data via `getImageData`.
- Conversion functions:
  - `convertASCII`, `convertBinary`, `convertBlocks`, `convertBraille`, `convertMatrix`, `convertEmoji`, plus `edgeDetect`.
- Updates “stats” (dimensions, chars generated, mode, render time) and output info (rows × cols).
- Output utilities:
  - **Copy** to clipboard
  - **Download** output as a `.txt`
  - **A+ / A-** to adjust output font size

## Notable implementation details
- Row count is derived from columns and image aspect ratio, with an **ASCII aspect correction factor (~0.55)** for most modes (emoji uses ~1.0).
- “Matrix” mode doesn’t map characters by density strongly; it mostly places spaces for dark pixels and random chars otherwise to create the aesthetic.
- “Colored output (ANSI-style)” is labeled as such, but the output is displayed as styled HTML text (not true ANSI sequences suitable for terminals).
