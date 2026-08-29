# 🏎️ REDLINE LAB — Vehicle Dynamics & Physics Simulator

![Redline Lab Banner](/api/placeholder/800/200) <!-- Add a screenshot of your app here later -->

REDLINE LAB is an interactive, high-performance web-based Vehicle Dynamics & Physics Simulation Engine. Built with plain-language vehicle customizers, real-time longitudinal numerical physics integration, a live 2D telemetry canvas, speedometer gauges, dual-car comparison mode, and dynamic braking safety matrix tables.

## 🚀 Join the Waitlist
Want early access to Redline or want to suggest new features? 
[**👉 Click here to fill out our Waitlist & Feedback Form**](https://forms.gle/McgMvV3XQ2FL3Kky9)

---

## ✨ Key Features
- **Futuristic HUD UI**: Dark mode glassmorphism dashboard powered by Orbitron, Rajdhani, JetBrains Mono, and Sora typography.
- **Real-Time Telemetry**: Live updating 2D canvas showing speed, RPM, and gear shifts.
- **Custom Vehicle Tuning**: Modify weight, engine torque, drag coefficient, and gear ratios on the fly.
- **Dual-Car Comparison**: Race two different setups against each other side-by-side.
- **Safety & Braking Matrix**: Dynamic calculation of stopping distances based on current speed and friction coefficients.

## 🛠️ Tech Stack
- **Frontend:** HTML5, CSS3 (Glassmorphism), Vanilla JavaScript / TypeScript, Canvas API
- **Backend/Database:** Supabase (PostgreSQL) for user data and garage queues.
- **UI Components:** Lucide Icons, Custom CSS variables for theming.

## ⚙️ Quick Start (Local Setup)

1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/redline.git
   ```
2. Navigate to the project directory:
   ```bash
   cd redline
   ```
3. Open `index.html` (or `getstart.html`) in your browser, or start a local dev server:
   ```bash
   npx serve .
   ```

---

## 🧮 Physics Engine: Formula Sheet

This section outlines the core longitudinal vehicle dynamics equations used in the Redline simulation engine. 

### 1. Engine & Drivetrain
Calculates the force actually pushing the car forward at the wheels.

*   **Wheel Torque ($T_{wheel}$):**  
    `T_wheel = Engine_Torque * Gear_Ratio * Final_Drive_Ratio * Drivetrain_Efficiency`
*   **Tractive Force ($F_{traction}$):**  
    `F_traction = T_wheel / Wheel_Radius`

### 2. Resistance Forces
The forces acting against the car's forward motion.

*   **Aerodynamic Drag ($F_{drag}$):**  
    `F_drag = 0.5 * Air_Density (ρ) * Velocity^2 * Drag_Coefficient (Cd) * Frontal_Area (A)`
    *(Air density is typically ~1.225 kg/m³ at sea level)*
*   **Rolling Resistance ($F_{rr}$):**  
    `F_rr = Rolling_Coefficient (Crr) * Mass * Gravity (9.81)`

### 3. Net Force & Acceleration (Newton's Second Law)
Calculating how much the car is actually speeding up or slowing down.

*   **Total Net Force ($F_{net}$):**  
    `F_net = F_traction - F_drag - F_rr`
*   **Acceleration ($a$):**  
    `a = F_net / Mass`  

*(Note: In higher accuracy sims, `Mass` is replaced by `Effective_Mass` which accounts for the rotational inertia of the wheels and engine).*

### 4. Integration (Velocity & Position)
How we update the car's speed and position every frame (Euler Integration).

*   **New Velocity ($V_{new}$):**  
    `V_new = V_old + (Acceleration * Delta_Time)`
*   **New Position ($X_{new}$):**  
    `X_new = X_old + (V_new * Delta_Time)`

### 5. Braking Dynamics
Calculating stopping distance and deceleration.

*   **Max Braking Force ($F_{brake\_max}$):**  
    `F_brake_max = Mass * Gravity * Tire_Friction_Coefficient (μ)`
*   **Deceleration during braking:**  
    `a_brake = - (F_brake_applied + F_drag + F_rr) / Mass`
*   **Stopping Distance ($d$):** (Derived from kinematics)  
    `d = Velocity^2 / (2 * |a_brake|)`

---

## 🤝 Contributing
Contributions, issues, and feature requests are welcome! Feel free to check the [issues page](https://github.com/yourusername/redline/issues) if you want to contribute.

## 📜 License
This project is licensed under the MIT License - see the LICENSE file for details. Educational Vehicle Dynamics Model.

