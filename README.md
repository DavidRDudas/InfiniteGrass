# Endless Hills

A calm-turning-eerie first-person walking experience for mobile (and desktop) browsers.
Rolling hills of freshly-cut grass stretch out forever between two white picket fences,
under a wide sky that drifts from a bright afternoon into a burning dusk and then the dark.
There's a house at the end of the lane — and it never comes any closer, as long as you keep
watching it.

Everything is generated live in the browser with **[Three.js](https://threejs.org/)** —
no asset files, no build step, one self-contained `index.html`.

## Play

Open `index.html` in any modern browser. On a phone, add it to your home screen for a
fullscreen experience. Tap **"Step Outside"** to begin (the tap also unlocks the audio —
headphones strongly recommended).

- **Left joystick** — walk in any direction.
- **Drag anywhere else** — look around (fully independent of moving).
- **♪ button** (top-right) — toggle sound.
- Desktop: **WASD / arrow keys** to move, **click-drag** to look.

## What's in it

- **Infinite terrain** — heights come from a pure noise function of world `(x, z)`; a single
  terrain mesh recenters on the player each frame for endless wandering.
- **Wind-swept grass** — instanced crossed-quad blades on a fixed world lattice, bent on the
  GPU by a fine gust plus a big rolling wind-wave that sweeps across the field and darkens the
  grass at its crest.
- **A living sky** — a slow day → dusk → night → dawn cycle drives the sky gradient, a sun and
  moon (with glowing discs), a star field at night, the fog colour/depth, the clouds, and all
  the scene lighting.
- **The walkable lane** — two parallel white picket fences (instanced and recycled, so they
  run to the horizon and ride the hills) with an open gate at the start.
- **The unreachable house** — pinned due north of the player. While you keep it in view it
  stays frozen and distant; the instant you look away it creeps closer, and never retreats —
  until you turn back and find it looming. A low dread stinger marks the reveal.
- **Atmosphere & life** — drifting fireflies/pollen motes (glowing after dark), a distant
  circling flock of crows, footsteps, occasional caws, and generative eerie ambient music
  (drone, breathing filter, wind, sparse echoing tones).
- **Cinematic post-processing** — bloom (the windows, sun, moon and fireflies glow), a subtle
  colour grade, vignette, and film grain, with ACES tone mapping.

## Notes

Performance scales with the device; the grass density, post-processing, and entity counts are
tuned to stay smooth on mid-range phones. If it runs hot on your device, the bloom pass is the
first thing to dial back.
