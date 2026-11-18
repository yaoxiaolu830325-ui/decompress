# Prism Break

A single-file arcade breakout game. Eight hand-built glass walls, a paddle with real english, five power-ups, chain scoring, and synthesized audio — no dependencies, no network, no build step.

Open `index.html` in any modern browser.

## Play

- **Move** — mouse, `←` `→` / `A` `D`, or drag on touch
- **Serve** — click, tap, or `Space`
- **Pause** — `P`, `Esc`, or the pause button
- **Sound** — `M` or the speaker button

## Design notes

- **Continuous collision:** the ball advances in ≤3-unit substeps with circle-vs-AABB resolution, so it survives 6000 u/s without tunnelling.
- **English:** outgoing angle blends paddle offset, paddle velocity and a decaying curve term. A minimum lateral component prevents dead vertical lanes; a watchdog shears any rally that goes 8 seconds without a brick.
- **Power-ups:** Wide (paddle), Multi (two extra balls), Slow (time warp), Catch (one sticky save), Life. 12% drop chance per destroyed brick.
- **Tuning:** ball speed ramps with level and destroyed bricks; hp2/hp3 bricks and steel rails appear from level 3.
- **Persistence:** best score and highest level reached live in `localStorage`, as does the audio preference.
- **Rendering:** procedural canvas art; brick tiles and the whole wall are cached, the background is pre-rendered, and the canvas is sized to device pixels (DPR capped at 2.5).
- **Accessibility:** full keyboard control, focus-visible styles, ARIA labels, and a reduced-motion mode that disables shake, trails and screen motion.
- **Responsive:** portrait phone layout, desktop layout, and a rotate prompt for short landscape phones.

All visuals are drawn with canvas primitives; all sound is synthesized with WebAudio. No images, fonts, libraries or CDN requests.
