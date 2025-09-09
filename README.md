# Auto-Crop White Background Images

A standalone HTML tool for quickly cropping white-background product or device images.  
It automatically finds the edges of the subject, trims excess white space, and adds a configurable margin. No backend required — everything runs in your browser.

👉 **[Use it live on GitHub Pages](https://benhar-dev.github.io/webtool-auto-white-crop/)**

---

## Features

- **Drag & Drop** images from your computer or directly from another webpage
- **Paste** (Ctrl/Cmd + V) images or image URLs
- **File picker** support (`.jpg`, `.png`, etc.)
- **Automatic white-background cropping** with configurable margin
- **Tolerance adjustment** for off-white or JPEG halo artifacts
- **Preview overlay** to visualize the detected crop box
- **Copy to clipboard** cropped image as PNG
- **Download** cropped image as PNG
- **Settings persistence** — remembers your margin/tolerance/preview toggle between sessions

## Quick Start

1. Open the [live GitHub Pages version](https://benhar-dev.github.io/webtool-auto-white-crop/).
2. Drag an image in, paste it, or enter a URL.
3. Adjust **Margin px** or **White tolerance** if needed.
4. Copy the cropped result to clipboard or download it as a PNG.

## Local Usage

If you prefer, you can run it locally:

1. Clone or download this repo.
2. Open `index.html` in your browser.
3. Use it the same way as the hosted version.

## Notes

- If the source website blocks CORS, dragging a URL directly may not allow pixel access. In that case, **paste** the image, or **save and drop** the file instead.
- Works entirely client-side. No uploads or external servers.

## Development

The core logic is in plain JavaScript:

- `AutoCropper.computeBounds()` finds the bounding box of non-white pixels
- `AutoCropper.cropWithMargin()` trims with the configured margin
- Settings are stored in `localStorage`

## License

MIT — free to use, modify, and distribute.
