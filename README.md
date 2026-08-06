# REDLINE LAB — Vehicle Dynamics & Physics Simulator

REDLINE LAB is an interactive, high-performance web-based Vehicle Dynamics & Physics Simulation Engine. Built with plain-language vehicle customizers, real-time longitudinal numerical physics integration, live 2D telemetry canvas, speedometer gauges, dual-car comparison mode, and dynamic braking safety matrix tables.

## ✨ Key Features

- **Futuristic HUD UI**: Dark mode glassmorphism dashboard powered by Orbitron, Rajdhani, JetBrains Mono, and Sora typography.
- **Real-Time Physics Engine**: Time-stepping Euler numerical solver ($\Delta t = 0.02\text{ s}$) calculating aerodynamic drag ($F_{\text{aero}}$), rolling resistance ($F_{\text{rolling}}$), slope grade ($F_{\text{hill}}$), and traction/power acceleration limits ($F_{\text{traction}}$).
- **Plain-Language Vehicle Customizer**: Pick Body Style, Weight Class (or exact kg override), Engine Power tier, Tire Grip grade, and Road Gradient slider ($-10^\circ$ to $+20^\circ$).
- **Dual-Car Comparison Mode**: Race `CAR A` vs `CAR B` side-by-side with winner badges (🏆), dual speedometer gauges, 2D race track rendering, and overlaid telemetry curves.
- **Live 2D Track Canvas**: Animated vector vehicle silhouettes with rotating spoked wheels, glowing headlights, launch smoke particles, live HUD readouts, and speed multipliers ($1\times, 2\times, 4\times$).
- **Telemetry Analytics (Chart.js)**: Multi-axis Speed ($\text{km/h}$) & Acceleration ($g$) graph synced with a live playback vertical timeline indicator line.
- **Braking Safety Matrix**: Calculates maximum advisable speeds ($\text{km/h}$ for $\le 60\text{ m}$ total stopping zone) and stopping distances across 5 road surface conditions (Dry Asphalt, Wet Asphalt, Gravel, Snow, Ice).

## 🛠️ Project Structure

```
├── index.html       # Full integrated Web Application (Landing Cover + HUD Simulator)
├── getstart.html    # Standalone Red Line cover landing page
├── README.md        # Project documentation
└── .gitignore       # Git ignore configuration
```

## 📜 License

MIT License. Educational Vehicle Dynamics Model.
