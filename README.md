# Freefall

Steer a skydiver down a twisting chasm whose walls narrow the deeper you go. Touch a
wall and you're squeezed — score is how far you fall.

Play it: **https://souravkundu.dev/labs/freefall/**

## Controls

- **← / →** or **A / D** to steer
- On touch: hold the **left / right** half of the screen
- **Space** or **tap** to drop, and to restart

## How it works

The chasm is a continuous function of depth: the gap meanders (layered sines) and its
width shrinks as you descend, while the fall speed ramps up. Collision samples a few
rows of the figure against the wall edges. Best depth is kept in `localStorage`. The
falling scream and the death shout are short clips (`scream.mp3`, `shout.mp3`) embedded
as base64 and decoded via the Web Audio API, so they play under the artifact's strict
content-security policy without any external requests; the impact thud is synthesised.

## Tech

Single self-contained HTML file, canvas-rendered. Vanilla JS, no dependencies, no build
step, no network calls — it runs offline. Part of
[Sourav Kundu · Labs](https://souravkundu.dev/labs/).

## Licence

MIT — see [LICENSE](LICENSE).
