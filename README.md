I am an Electrical Engineering undergraduate at UPI Bandung specializing in Telecommunications, Embedded Systems, and Control Logic. Below is a detailed breakdown of my key engineering projects.

---

## Aerospace PID Control Simulation

**Role:** Lead Developer  
**Tools & Technologies:** MATLAB, Simulink, Python, Kerbal Space Program (KSP), kOS   
**Focus:** Closed-Loop Control Systems, Flight Dynamics, Telemetry Processing  

### 1. Objective
To design and simulate a closed-loop PID (Proportional-Integral-Derivative) control system capable of autonomously managing a rocket's launch trajectory and executing a propulsive, thrust-vectored landing sequence (similar to the Falcon 9). 

### 2. System Architecture & Control Logic
The core challenge of this project was maintaining the rocket's stability against atmospheric drag and gravity during descent. The system relies on real-time telemetry data to adjust engine thrust and gimbal angles.

* **Proportional (P):** Calculates the immediate error between the current altitude/velocity and the target landing parameters.
* **Integral (I):** Accumulates past errors to correct steady-state offsets (ensuring the rocket doesn't hover just above the pad).
* **Derivative (D):** Predicts future errors based on the rate of descent, preventing overcorrection and catastrophic lithobraking (crashing).

![Simulink Block Diagram](assets/simulink.png)

### 3. Simulation Environment (Hardware-in-the-Loop Concept)
To test the control logic without a physical rocket, I first designed the simulation in MATLAB, then moved to 3D simulation in KSP by using kOS as it's automated script controller. KSP acted as the physics engine, feeding real-time altitude, velocity, and pitch data to the controller, which then sent throttle and steering commands back to kOS.

![KSP Simulation](assets/Kerbal.jpeg)

### 4. Results & Telemetry
The finely tuned PID controller successfully stabilized the descent vector and managed the suicide-burn timing, resulting in a fully autonomous, soft touchdown. 
The blue line shows the altitude of the rocket, while the yellow line shows the velocity of the rocket, as the rocket gets closer to the ground, the rocket would fall slower and finally lands softly.
![Telemetry Graph](assets/result.png)

---
