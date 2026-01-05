# OrbitSim_new
3D Orbit Simulator
A high precision, interactive N-body gravity simulation of the Solar System built for the club project. This simulator visualizes real orbital mechanics using a custom physics engine to demonstrate gravitational perturbation and conservation laws.
https://blaze505050.github.io/OrbitSim_new/ 
This project simulates the motion of celestial bodies using the Velocity Verlet integration method. Unlike standard Euler integration, this symplectic integrator preserves the system's energy over long durations, allowing for stable orbits that don't spiral out of control.
The simulation runs in a full 3D environment, allowing users to inspect orbital inclinations, visualize velocity changes at perihelion/aphelion, and monitor system stability via real-time analytics.
Features
1. Physics Engine
N Body Gravity: Calculates gravitational forces between all pairs of bodies ($O(n^2)$ complexity).
Symplectic Integration: Uses the Velocity Verlet algorithm for energy conservation.
Real Data Initialization: Planets are initialized using semi major axis, eccentricity, and inclination data.
2. Interactive 3D Visualization
Render Engine: Built with Three.js for hardware-accelerated 3D graphics.
Camera System: Smart "Chase Camera" that smoothly locks onto and follows any target body (Sun, Earth, Jupiter, etc.).
Dynamic Trails: Visualizes orbital paths to show history and curvature.
3. Mission Analytics Dashboard
A real time data overlay (toggleable via UI) that plots:
Total System Energy: Demonstrates conservation of energy ($\Delta E \approx 0$).
Angular Momentum: Verifies rotational stability.
Live Telemetry: Tracks the distance ($r$) and velocity ($v$) of the focused planet, visualizing Kepler's 2nd Law (planets move faster when closer to the Sun).
🎮 Controls
Action
Mouse / Trackpad
Touchscreen
Rotate View
Left Click + Drag
One finger Drag
Pan View
Right Click + Drag
Two finger Drag
Zoom
Scroll Wheel
Pinch Zoom
Focus Planet
Click buttons in UI
Tap buttons in UI
Toggle HUD
Click "Open Analytics"
Tap "Open Analytics"
🛠️ Tech Stack
Language: Vanilla JavaScript (ES6+)
Rendering: Three.js (r128)
Styling: CSS3 (Glassmorphism UI)
Hosting: GitHub Pages
📦 How to Run Locally
Clone this repository:
Navigate to the folder.
Open index.html in any modern web browser (Chrome, Firefox, Edge, Safari).
No installation, build steps, or server required!

Built for the Astronomy & Astrophysics Club (AAC) NITK.
