# Gravitational Dynamics Simulator

A single-file, interactive 3D simulator for celestial mechanics and relativity visualization. It combines an educational HUD, cinematic camera modes, and real-time overlays to explore orbits, curvature, and mission story presets — all in the browser.

## Why This Matters

- Visualizes spacetime curvature and orbital stability with an intuitive overlay and rings
- Explains gravity and relativity concepts through direct interaction
- Offers curated scenarios (Solar System, Galaxy cores, TRAPPIST-1, Lagrange points) for quick learning
- Exports scenes with embedded legend for presentations and portfolios

## Quick Start (Windows)

- Prerequisite: Python 3
- Run a local server from the project directory:

```powershell
cd "C:\Users\hp\Documents\trae_projects\Gravitational Dynamics Simulator"
python -m http.server 4173
```

- Open http://localhost:4173/ in your browser
- If “Service Unavailable”, hard refresh (Ctrl+F5) or try http://127.0.0.1:4173/

## Core Features

- Relativity Overlay
  - Colors spacetime grid by curvature; dims non-relativistic objects
  - Toggle in Parameters; keyboard: o
- Curvature Heatmap
  - Glowing halo around the selected body tied to curvature index
- Orbital Stability Rings
  - Dotted inner/outer rings based on Hill sphere
- Camera Modes
  - Free, Follow, Chase, God’s Eye; keyboard: f, c, g
- Instrument FOV
  - Spacecraft field-of-view rectangle aligned to velocity; toggle in Parameters
- Snapshot Export
  - Saves canvas PNG with legend (scenario, date, selection, curvature/time dilation); keyboard: s
- Session Persistence
  - Save/Load with Auto-Load to resume exactly where you left off
- Templates
  - Solar System, Galaxy, Black Hole, M87* Jet, Runaway SMBH, TRAPPIST-1, Lagrange Points

Code entry point: [index.html]

## Controls

- Rotate: Right-click + drag
- Pan: Left-click + drag (when not locked)
- Zoom: Mouse wheel
- Select: Click bodies in the “Celestial Database” panel
- Keyboard
  - o: Relativity Overlay
  - g: God’s Eye
  - f: Follow (or Free if nothing selected)
  - c: Chase
  - h: Help modal
  - s: Snapshot export

## Panels & UI

- Left: Parameters, Camera Mode, Snapshot, Help, Session controls
- Right: Target panel (appears when a body is selected), Celestial Database with search and “Pin Selected to Top”
- JWST Live
  - Compact button in Target panel
  - Floating button bottom-right for quick access

## Data & Ordering

- Sun appears under Stars (top of group)
- Planet order: Mercury → Venus → Earth → Mars → Jupiter → Saturn → Uranus → Neptune
- Moons listed under their parent planet, following parent order
- Spacecraft grouped by parent: Spacecrafts: Earth, Spacecrafts: Jupiter, Spacecrafts: Saturn; others under Spacecrafts
- Search filter narrows the Celestial Database list by name

## Usage Tips

- Start with “Solar System”; select planets and spacecraft to see rings, heatmap, and FOV
- Try “God’s Eye” for a system overview; “Follow/Chase” for cinematic tracking
- Toggle Relativity Overlay to focus on curvature
- Use Snapshot to export scenes with a legend

## Troubleshooting

- Service Unavailable
  - Hard refresh (Ctrl+F5)
  - Restart server: ensure you’re in the project directory before running

- UI appears stale
  - Clear browser cache or open an incognito window

## Extend

- Add bodies: modify SOLAR_DATA and SOLAR_MOONS in [index.html]
- Create new templates: follow existing template functions (e.g., TRAPPIST-1, Lagrange Points) and call `buildNavMenu()` after populating `bodies`

## Security

- No secrets or keys stored; all data is local and static

## License

- See LICENSE in the repository (if present)
