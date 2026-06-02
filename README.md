# Endless Hills

A calm, slightly eerie first-person walking experience for mobile (and desktop) browsers.
Rolling hills of freshly-cut grass stretch out forever under a wide blue sky dotted with
fluffy white clouds. There's no goal and no edge — just wander.

## Play

Open `index.html` in any modern browser. On a phone, host it somewhere (or open the file
locally) and add it to your home screen for a fullscreen experience.

- **Tap "Step Outside"** to begin (this also starts the music — mobile browsers require a tap).
- **Left joystick** — walk in any direction.
- **Drag anywhere else** — look around.
- **♪ button** (top-right) — toggle the music.
- Desktop: **WASD / arrow keys** to move, **click-drag** to look.

## How it works

Everything is generated in the browser with **[Three.js](https://threejs.org/)** — no
asset files, no build step, one self-contained HTML file.

- **Infinite terrain** — heights come from a pure noise function of world `(x, z)`, so the
  world is deterministic and endless. A single terrain mesh recenters on the player each
  frame and re-samples the height field.
- **Grass** — instanced crossed quads placed on a fixed world lattice so blades keep their
  position as the field scrolls beneath you (no popping or swimming).
- **Sky & clouds** — a gradient sky dome plus drifting, procedurally-painted cloud billboards
  that wrap around the player so they always feel infinitely far away.
- **Eerie music** — generated live with the Web Audio API: a low drifting drone with a
  breathing low-pass filter, soft filtered wind, and sparse, echoing high tones in a minor
  scale.

## Notes

Headphones are recommended for the ambience. Performance scales with device — the grass
density and terrain resolution are tuned to stay smooth on mid-range phones.
