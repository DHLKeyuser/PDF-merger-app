## DHL PDF Merger with Drag & Drop Sorting

A lightweight, client‑side web app to merge multiple PDF files into a single document. Files are handled entirely in your browser—nothing is uploaded—so it’s fast and privacy‑friendly. The UI supports drag‑and‑drop, sortable reordering, quick preview, and a custom output filename.

### Features
- **Drag & drop PDFs**: Add multiple PDFs or use the Select PDFs button.
- **Smart initial sort**: Files are initially sorted alphanumerically by name.
- **Reorder by dragging**: Use drag‑and‑drop to change the merge order.
- **Preview quickly**: Open any selected PDF in a new tab to verify contents.
- **Remove items**: Remove individual PDFs or clear the entire list.
- **Custom output name**: Set the merged file name (defaults to "DN Consolidation").
- **Local processing only**: Merging happens in the browser via `pdf-lib`; no uploads.
- **Simple, single‑file app**: All HTML/CSS/JS is in `index.html`.

### Tech stack
- **Vanilla HTML, CSS, JavaScript** (no build step)
- **[pdf-lib](https://pdf-lib.js.org/)** for PDF manipulation in the browser
- **[SortableJS](https://github.com/SortableJS/Sortable)** for drag‑and‑drop list reordering

### Getting started
- **Option A (simplest)**: Double‑click `index.html` to open it in a modern browser.
- **Option B (serve locally)**:
  - Using Python 3:
    ```bash
    python -m http.server 8000
    ```
    Then open `http://localhost:8000/` and click `index.html`.
  - Using Node.js:
    ```bash
    npx serve -l 8000
    ```
    Then open `http://localhost:8000/` and click `index.html`.

### Usage
1. **Add PDFs**: Drag and drop PDFs into the drop area or click "Select PDFs".
2. **Reorder**: Drag items in the list to set the final merge order.
3. **Preview** (optional): Click "Preview" on a file to open it in a new tab.
4. **Remove** (optional): Remove individual files or click "Remove All" to clear.
5. **Set name**: Enter your desired merged filename in the "Filename" input.
6. **Merge**: Click "Merge PDFs" to download the combined PDF.

### Privacy and security
- All processing occurs **locally in your browser** using Object URLs and `pdf-lib`.
- No PDFs are uploaded to a server.

### Project structure
- `index.html` — Single‑page app with inline CSS and JavaScript, loading `pdf-lib` and `SortableJS` via CDN.

### Notes and limitations
- **Large files**: Merging very large PDFs or many files can be memory‑intensive in the browser and may take time.
- **Whole‑file merge**: Page‑level reordering/extraction isn’t supported; the app merges full PDFs.
- **Browser support**: Works on modern browsers (Chrome, Edge, Firefox). Internet Explorer is not supported.
- **CDN availability**: The app pulls libraries from CDNs. For offline or restricted environments, vendor the dependencies locally.

### Customization
- Replace the logo/link in `index.html` to match your organization.
- Extract inline CSS/JS into separate files if you prefer a modular structure.
- Add validation, progress indicators, or error reporting as needed.

### Acknowledgements
- Built with [pdf-lib](https://pdf-lib.js.org/) and [SortableJS](https://github.com/SortableJS/Sortable).
- DHL trademarks and logos are the property of DHL.

### License
Specify a license for this repository (e.g., MIT, Apache‑2.0) or add a `LICENSE` file.
