# NIGHTDRIVE · 夜行

A pseudo-3D neon highway racer in a single HTML file. No install, no account, no ads, no external assets — road, cars, skyline, engine note and music are all generated in code.

**How to play**

- `W` / `↑` throttle, `S` / `↓` brake, `A` `D` / `←` `→` steer, `P` pause, `R` restart, `M` sound
- On touch devices: on-screen steer pads bottom-left, brake/gas bottom-right
- Hold speed through the curves, thread the traffic, reach the distance gate before the clock dies

**What's in it**

- Three stages with their own palette, skyline and corner profile: Neon Harbor → Sunset Coast → Void Canyon
- Pseudo-3D road with curves, crests, banking haze and per-segment fog
- Traffic AI: lane drift, rolling two-wide blocks, recycled traffic so the road never empties out
- Collision recovery: shunt + 1.1 s invulnerability, off-road grip loss, barrier scrapes
- Scoring: distance rate × combo multiplier, near-miss bonuses, stage-clear time bonus; best run persisted in `localStorage`
- Procedural WebAudio: engine, wind, crash, near-miss whoosh, stage fanfare and a low synth pulse — toggle with the speaker button
- Responsive HUD (desktop / phone portrait / phone landscape / tablet), pause on tab blur, reduced-motion support

Built by Yao Engineering — [engineering calculation tools](https://ko-fi.com/yaoengineering).

Licence: MIT for the code.
