# ForzaClone: Horizon Circuit

A browser-based 3D racing game built with Three.js. Drive a procedural circuit, race against AI drivers, drift for skill points, use NOS and Blur-style power-ups, and rewind the last few seconds of the race.

The start menu includes a world tour of eleven circuits — Horizon, Monaco, Monza,
Silverstone, Spa, Suzuka, Bahrain, Imola, Zandvoort, COTA, and Interlagos — six
selectable cars, a weather selector, and a choice of 1, 2, 3, 5, or 10 laps.
Races start with a five-light F1 gantry, run through DRS zones, and end at the
start/finish line with a results screen.

## Play locally

The game uses ES modules, so open it through a local web server rather than opening `index.html` directly.

With Python installed:

```powershell
py -m http.server 8000
```

Then open <http://localhost:8000> in a browser.

You can also use any static web server, such as the VS Code Live Server extension.

## Controls

| Key | Action |
| --- | --- |
| `W` / `Arrow Up` | Accelerate |
| `S` / `Arrow Down` | Brake or reverse |
| `A` / `Arrow Left` | Steer left |
| `D` / `Arrow Right` | Steer right |
| `Space` | Drift / handbrake |
| `Shift` | NOS boost |
| `E` | Use held power-up |
| `R` | Rewind |
| `Esc` / `P` | Pause |
| `C` | Toggle commentary |

The start menu lets you pick between six cars with different top speed,
acceleration, and handling, including the open-wheel APEX F1 formula car. You can
also enter a driver name, which is saved along with your race time. The pause
menu offers resume, restart, changing venue/car, and quitting to the main menu.

Each race ends with a results card showing your finish, total time, best lap,
and top speed, plus a leaderboard for that circuit and lap count. The top eight
times are listed (fastest first) and the run you just completed is highlighted.
Times and the driver name persist in `localStorage` (`forzaLeaderboard` and
`forzaDriverName`).

Circuits have wide roads, grandstand crowds, trackside fans, venue-themed
buildings, and trees. F1 venues add five-light starts and DRS zones that open the
rear wing and lift top speed on the straights. The weather can be fixed or left
on AUTO, where conditions cycle between clear, overcast, rain, and fog. Rain adds
trackside particles, darkens the surface, and cuts grip, while fog reduces
visibility. A race commentator calls the start, final lap, overtakes, near
misses, wall contact, big drifts, fastest laps, boost use, DRS, weather changes,
and the finish. Trade paint with AI, bank drift points, and use the NOS/ERS boost
to climb the order.

Glowing power-up pads are placed around every circuit and respawn after a short
delay. Drive through one to fill the item slot, then press `E` to fire it. The
seven pickups are NITRO (instant boost and full NOS), SHUNT (homing missile that
slows the car ahead), BOLT (three forward projectiles), MINE (drops behind to
catch a pursuer), SHIELD (blocks incoming shunts for 6.5 seconds), SHOCK (slows
every rival ahead), and REPAIR (clears a hit, refills NOS, and grants a short
shield). Rival drivers can fire shunts back at you, so keep a shield ready or use
repair to recover.

## Technology

- HTML, CSS, and JavaScript
- Three.js `0.160.0`
- WebGL post-processing with bloom
- Procedural track, terrain, scenery, open-wheel and GT vehicles, weather, HUD, and arcade power-ups

## Notes

This is an original fan-made racing prototype for learning and experimentation. It is not affiliated with or endorsed by Microsoft or the Forza franchise. Three.js is loaded from the public `unpkg.com` CDN at runtime, so an internet connection is required unless the dependency is self-hosted.
