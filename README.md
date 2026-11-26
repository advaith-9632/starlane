# Starlane

A slow, good-looking space flight game that runs in the browser on desktop and iPad.

Fly freely in 3D through open space. The route is marked by glowing rings, a drifting stream of light and a tunnel of asteroids, but you can wander anywhere.

## Modes

- **Cruise**: an endless route with no clock. Turn on autopilot to sit back and watch.
- **Time Trial**: a random course of 18 rings. Each missed ring adds 2 seconds. Your best run is saved on the device and replays as a ghost. Every course has a short code you can share to race the same one.

There are five skies to switch between: Nebula Drift, Amber Reach, Glacier Belt, Aurora Void and Crimson Giant.

## Controls

**Keyboard** (all of these can be changed under *Change keyboard controls* in the menu):

| Action | Default key |
| --- | --- |
| Thrust / brake | W / S |
| Turn | A / D or ← / → |
| Climb / dive | ↑ / ↓ |
| Boost | Shift or Space |
| Camera (chase, cockpit, cinematic) | C |
| Change sky | E |
| Autopilot (Cruise) | P |
| Restart run (Time Trial) | R |
| Pause | Esc |

**iPad / touch**: the joystick on the left turns and climbs. Thrust, Brake and Boost are on the right.

## Running it locally

It's a single `index.html` with no build step. Three.js loads from a CDN, so you need to be online.

```
node serve.mjs
```

Then open http://localhost:8137.
