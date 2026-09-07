# Evidence (source: BdonCatanHand.html, 6712 bytes)
## Structural
- Interactive elements: 10 cards x 2 buttons + Roll + Reset = 22 (lines 73, 54, 57)
- Max nesting depth: body > .grid > .card > .ctl > button = 4
- Repeated pattern: +/- pair x10, same purpose, one template (line 67-75) — OK
- Dead code: none
## Visual (INFERRED from CSS)
- Spacing values used: 4, 6, 8, 10, 12, 14, 22, 28 px (lines 14-17, 22, 28, 36) — no scale
- Type sizes: .72, .9, 1.05, 1.2, 1.4, 1.8, 1.9, 2.2, 2.4 rem — 9 sizes, no scale
- Distinct colors: 20+ hex tokens
- Contrast (measured): white on brick 3.97, white on lumber 4.25, white on ore 3.50 — label text at .72rem/opacity .9 FAILS WCAG AA (4.5). Wool 7.98, grain 7.77, dev 5.79 pass.
- States: focus = browser default only (line 23 border:0, no :focus-visible); disabled = missing (minus at 0 silently no-ops, line 91); reduced-motion = not respected (line 31-32); error = localStorage JSON.parse unguarded (line 65); empty = "0" shown, fine; loading = n/a
## Copy & Honesty
- Strings: "Catan Hand", "Resources", "Development Cards", "Total resource cards:", "Roll", "Reset hand", confirm "Reset your whole hand to zero?" — all literal, no inflation, no dark patterns
- +/- buttons have no accessible name beyond the glyph (line 73)
## Weight & Friction
- JS: ~1.6 KB inline; requests: 1 HTML + 1 Google Fonts CSS + 1-2 woff2 (line 12, render-blocking @import)
- Idle animations: 0; modals on load: 0
## Accessibility
- meta viewport maximum-scale=1 blocks pinch zoom (line 6) — WCAG 1.4.4 fail
- No landmarks (no main/section/footer); count changes not announced
- Keyboard: all buttons reachable; focus ring is browser default over 4px white borders
