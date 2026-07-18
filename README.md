# Lottie2SVG

Extract any frame from a Lottie animation and download it as an SVG.

Lottie2SVG is a small, browser-based tool that supports both Bodymovin JSON files and packaged `.lottie` files. Everything runs locally in the browser.

## Features

- Drag-and-drop file loading
- Supports `.json` and `.lottie`
- Interactive SVG preview
- Export the first, last, or any selected frame
- Embedded image support for packaged `.lottie` files
- No upload or server-side processing
- Responsive, single-page interface

## Usage

1. Open the page in a browser.
2. Drop a `.json` or `.lottie` file onto the upload area.
3. Enter the frame number to extract.
4. Click **Download selected frame**.

The exported file is named:

```text
<animation-name>-frame-<frame-number>.svg
```

## Run locally

Because the page loads a default animation using `fetch`, serve the repository through a local HTTP server rather than opening the HTML file directly.

```bash
python -m http.server 8000
```

Then open:

```text
http://localhost:8000
```

## GitHub Pages

For GitHub Pages, rename `lottie2svg.html` to `index.html`, then enable Pages:

1. Open the repository settings.
2. Go to **Pages**.
3. Select **Deploy from a branch**.
4. Choose the branch and root directory.

The site will be available at:

```text
https://<username>.github.io/lottie2svg/
```

## Default animation

The page currently attempts to load:

```text
./earthengineStudio.json
```

Place that file beside the HTML page, or remove the default `lottie.loadAnimation(...)` block if the application should start empty.

## Dependencies

Loaded from public CDNs:

- [Lottie Web](https://github.com/airbnb/lottie-web)
- [fflate](https://github.com/101arrowz/fflate)

## Browser support

A modern browser with support for:

- ES2017+
- `File`
- `Blob`
- `URL.createObjectURL`
- `requestAnimationFrame`
- SVG rendering

## Privacy

Animation files are processed entirely in the browser and are not uploaded by this application.

## License

Add the license of your choice, for example [MIT](https://opensource.org/license/mit).
