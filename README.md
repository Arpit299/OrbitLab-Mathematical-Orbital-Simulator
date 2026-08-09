# OrbitLab: Mathematical Orbital Simulator

![N-Body Dynamics](https://img.shields.io/badge/Physics-N--Body-blue)
![Python](https://img.shields.io/badge/Python-3.8%2B-green)

A robust Python-based framework for simulating complex gravitational systems using high-precision numerical integration. 

## 🚀 Features

*   **N-Body Engine**: Simulate an arbitrary number of gravitational bodies.
*   **RK4 Integration**: Utilizes the 4th-order Runge-Kutta method for superior stability and energy conservation compared to Euler methods.
*   **Versatile Scenarios**: Pre-configured for:
    *   Earth-Moon dynamics.
    *   Stable binary star systems.
    *   Chaotic three-body problems.
    *   Low Earth Orbit (LEO) satellite trajectories.
*   **Physics Analysis**: Built-in tracking for velocity magnitudes and total mechanical energy (Kinetic + Potential) to verify physical accuracy.

## 🛠️ Installation & Usage

```python
# Define your bodies
earth = Body("Earth", 5.972e24, np.array([0.0, 0.0, 0.0]), np.array([0.0, 0.0, 0.0]), "blue")
moon = Body("Moon", 7.348e22, np.array([384.4e6, 0.0, 0.0]), np.array([0.0, 1022.0, 0.0]), "gray")

# Initialize and run simulation
sim = OrbitSimulator([earth, moon])
sim.run(duration=2592000, dt=3600)
```

## 📊 Physics Verification

The engine ensures energy conservation, a critical metric for long-term orbital stability. The `plot_physics` utility allows for real-time monitoring of system energy fluctuations.

## 📜 Requirements

- `numpy`
- `matplotlib`
- `dataclasses` (Standard Library in Python 3.7+)

---
