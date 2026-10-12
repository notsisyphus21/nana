# ForzaClone: Horizon Circuit

A browser-based 3D racing game built with Three.js. Drive a procedural circuit, race against AI drivers, drift for skill points, use NOS, and rewind the last few seconds of the race.

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
| `R` | Rewind |

## Technology

- HTML, CSS, and JavaScript
- Three.js `0.160.0`
- WebGL post-processing with bloom
- Procedurally generated track, terrain, scenery, vehicles, particles, and HUD

## Notes

This is an original fan-made racing prototype for learning and experimentation. It is not affiliated with or endorsed by Microsoft or the Forza franchise. Three.js is loaded from the public `unpkg.com` CDN at runtime, so an internet connection is required unless the dependency is self-hosted.
