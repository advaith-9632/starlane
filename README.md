# Starlane

A slow, good-looking space flight game that runs in the browser on desktop, iPad and with a controller.

Fly freely in 3D through open space. The route is marked by glowing rings, a drifting stream of light and a tunnel of asteroids, but you can wander anywhere.

## Modes

- **Cruise**: an endless route with no clock. Turn on autopilot to sit back and watch.
- **Time Trial**: a random course of 18 rings. Each missed ring adds 2 seconds. Your best run is saved on the device and replays as a ghost. Every course has a short code you can share to race the same one.
- **Race friends**: one person creates a room and shares the 4-letter code; everyone else joins on their own device and races the same course live.
- **Hangar**: spend coins on upgrades (boost tank, boost power, shield, engine), weapons (twin blaster, scatter gun, heavy cannon) and looks (hull shape, paint, engine glow).

## Things in space

- **Rings** recharge a little shield and boost. **Speed rings** (with arrows) fire you forward.
- **Asteroids** have health based on their size. Your guns lock on to the rock in front of you automatically; small ones also break if you ram them at boost speed, at a cost to your shield.
- **Shield**: crashing drains it. At zero you get a hull breach and stall for a moment.
- **Pickups**: coins, shield cells (green) and overdrive (orange, unlimited boost for 5 seconds).
- **Boost** locks out when you run it dry and comes back once it refills to 30%. **Jumps** throw you about 30 m straight up or down for 20% boost, with a 1.6 s cooldown.

There are nine skies: Nebula Drift, Amber Reach, Glacier Belt, Aurora Void, Crimson Giant, Ion Storm, Rose Quartz, Event Horizon and Coral Reef. Each has its own music key.

## Controls

**Keyboard** (all changeable under *Controls and sound* in the menu):

| Action | Default key |
| --- | --- |
| Thrust / brake | W / S |
| Turn | A / D or ← / → |
| Climb / dive | ↑ / ↓ |
| Boost | Left Shift |
| Fire | F or Enter |
| Jump up / down | Space / X |
| Camera (chase, cockpit, cinematic) | C |
| Change sky | E |
| Autopilot (Cruise) | P |
| Restart run (Time Trial) | R |
| Pause | Esc |

**Controller** (Xbox / PlayStation layout): left stick steers and climbs, RT thrust, LT brake, A boost, X fire, RB / LB jump, Y camera, View sky, Start pause. The D-pad and A / B work in menus.

**iPad / touch**: two layouts (*Flight stick* or *Keyboard style*), and every button can be dragged to a new spot with *Move buttons*.

Steering sensitivity, music and effects volume are in the same settings panel.

## Running it locally

It's a single `index.html` with no build step. Three.js loads from a CDN, so you need to be online.

```
node serve.mjs
```

Then open http://localhost:8137.

Multiplayer passes messages through a free public MQTT relay (EMQX, with HiveMQ as a fallback) over a secure WebSocket, so devices never need a direct connection. Room traffic is public on that relay, so only player names and ship positions are sent.
