# Muhammad Hadi Baihaqie - Engineering Portfolio

Welcome to my portfolio! I am an Electrical Engineering undergraduate at UPI Bandung specializing in Telecommunications, Embedded Systems, and Control Logic. Below is a detailed breakdown of my key engineering projects.

---

## 🚀 Aerospace PID Control Simulation

**Role:** Lead Developer  
**Tools & Technologies:** MATLAB, Simulink, Kerbal Space Program (KSP), kRPC, Python  
**Focus:** Closed-Loop Control Systems, Flight Dynamics, Telemetry Processing  

### 1. Objective
To design and simulate a closed-loop PID (Proportional-Integral-Derivative) control system capable of autonomously managing a rocket's launch trajectory and executing a propulsive, thrust-vectored landing sequence (similar to the Falcon 9). 

### 2. System Architecture & Control Logic
The core challenge of this project was maintaining the rocket's stability against atmospheric drag and gravity during descent. The system relies on real-time telemetry data to adjust engine thrust and gimbal angles.

* **Proportional (P):** Calculates the immediate error between the current altitude/velocity and the target landing parameters.
* **Integral (I):** Accumulates past errors to correct steady-state offsets (ensuring the rocket doesn't hover just above the pad).
* **Derivative (D):** Predicts future errors based on the rate of descent, preventing overcorrection and catastrophic lithobraking (crashing).

> 📸 *(Insert a screenshot of your MATLAB/Simulink block diagram here)* > `![Simulink Block Diagram](assets/pid_simulink.png)`

### 3. Simulation Environment (Hardware-in-the-Loop Concept)
To test the control logic without a physical rocket, I bridged MATLAB/Python with Kerbal Space Program using the kRPC server. KSP acted as the physics engine, feeding real-time altitude, velocity, and pitch data to the controller, which then sent throttle and steering commands back to the simulation.

> 📸 *(Insert a screenshot of the rocket landing in KSP, maybe with the kRPC terminal open next to it)* > `![KSP Simulation](assets/ksp_landing.png)`

### 4. Results & Telemetry
The finely tuned PID controller successfully stabilized the descent vector and managed the suicide-burn timing, resulting in a fully autonomous, soft touchdown. 

## 📡 Wireless Sensor Network (WSN) & Custom IoT Dashboard

**Role:** Full-Stack Hardware & System Developer  
**Tools & Technologies:** ESP32, nRF24L01, GPS Modules, C/C++, Web/Dashboard Frameworks  
**Focus:** RF Communication, Network Topology, Telemetry Visualization, Anti-Interference Logic  

### 1. Objective
To architect and deploy a robust, multi-node Wireless Sensor Network capable of acquiring real-time GPS telemetry and transmitting it securely to a custom-developed, centralized IoT dashboard for live tracking and data logging.

### 2. System Architecture & Network Topology
The system was designed using a star-network topology. Remote sensor nodes aggregate physical coordinate data via GPS and transmit it wirelessly to a central microcontroller gateway. The gateway then processes the incoming RF packets and pushes the telemetry to a web-based dashboard.

> 📸 *(Insert a clean block diagram showing Node 1, Node 2 -> Gateway -> Cloud/Dashboard)* > `![Network Topology](assets/wsn_topology.png)`

### 3. Hardware & Communication Logic (Frequency Hopping)
Because the 2.4GHz band is highly congested, static-channel transmission is prone to packet loss and interference. To solve this, I programmed a custom Frequency Hopping Spread Spectrum (FHSS) algorithm for the nRF24L01 modules.
* **Nodes and the Gateway synchronously change RF channels** based on a pre-defined algorithmic sequence.
* This ensures high-reliability data transmission even in noisy RF environments (a core principle in secure and industrial telecommunications).

> 📸 *(Insert a photo of the physical sensor nodes and the nRF24 wiring)* > `![Hardware Setup](assets/nrf24_nodes.png)`

### 4. Custom IoT Dashboard & Data Visualization
Rather than relying on generic third-party platforms, I developed the IoT dashboard from the ground up to handle the incoming data streams. 
* The dashboard parses the payload and visualizes the GPS coordinates, node status, and signal reliability in real-time.

> 📸 *(Insert a screenshot of your actual IoT Dashboard UI showing the map or data logs)* > `![IoT Dashboard UI](assets/iot_dashboard.png)`

---
> 📸 *(Insert a graph/plot from MATLAB or Python showing the altitude vs. velocity over time during the landing)* > `![Telemetry Graph](assets/telemetry_plot.png)`

---

*(You can add the next project, like your WSN & IoT Dashboard, right below this line!)*
