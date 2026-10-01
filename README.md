# Flux: Liberty Express website test area

Staging workflow for trying website ideas on a copy of the Liberty Express Weebly theme ("Liberty_I", based on Weebly's stock Venue theme) before touching the live site.

## Layout
- `baseline/Liberty1_1/`: untouched theme export. Rollback copy. Never edit.
- `patches/NN-name/`: one folder per idea: `*.diff` (review), `files/` (full changed files, paste-ready), notes.

## Workflow (one idea at a time)
1. Duplicate the live Weebly site (verify the copy includes the custom theme; keep it off the live domain and out of search engines).
2. Paste the patch's `files/` into the duplicate's Code Editor. Save there only.
3. Check the preview: header, store/cart, member login, footer form, mobile slide-out menu, gallery swipe on a real touch device, contrast.
4. If it passes, paste the same files into the live theme. Record the result in the patch folder.
5. Rollback: re-paste the matching files from `baseline/`.

Note: whether Weebly accepts a theme ZIP re-import on an existing site is unverified. Pasting the changed files is the supported path used here.

## Patches
- `01-navy-gold`: navy/gold palette preset, `@body-bg`/`@card-bg` variables replace three hardcoded `#0f0f1a`, lighter footer form-label text, Fancybox swipe fix (no recursive rebinding). Changed files: `manifest.json`, `styles/variables.less`, `styles/main.less`, `assets/custom.js`.

## Open items
- `popout.html` is unfinished (CSS only, no markup/script; starts at opacity 0). Needs markup, a toggle script and `pointer-events: none` on the base rule before use.
- Gallery swipe fix needs a real touch-device test.
