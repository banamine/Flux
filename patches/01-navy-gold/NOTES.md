# 01-navy-gold: verification status
- Applied to the export by script; all line anchors matched (main.less 40, 1408, 1413; footer greys 1403, 1412).
- `custom.js` passes a JS syntax check.
- LESS compile test (local lessc, Weebly-injected variables stubbed): patched variables resolve, no `#0f0f1a` remains. The untouched baseline also fails local lessc on odd spacing (`td : nth-child`, `: :after`), so Weebly's own compiler is the real test: paste on a duplicate site and check for compile errors.
- NOT verified: live Weebly preview, touch-device swipe, contrast in the rendered pages.
- Left alone on purpose: `#626262` at main.less 1283, 1341, 1373 (site-wide form/search text on light content).
