# 🤖 Line-Following Robot – Follower RC

## 📝 Overview
This project is a **PID-controlled autonomous line-following robot** built on the **Arduino Mega 2560 (ATmega2560)** platform.  
The system integrates analog photoresistor feedback, motor driver control (L298N), and real-time PID tuning via potentiometers to achieve smooth, responsive path tracking and stable navigation at high speed.

---

## 👥 Team Members
* Genaro Salazar  
* Nathan Davis  
* Gordon Yang  
* Hussain Alrammadan  

---

## 🏆 Key Features & Achievements

* **🏁 Competition Winner:** Placed **first in all track challenges**, including timed sprints and complex curved-path navigation.  

* **Adaptive PID Control with Battery-Aware Scaling:**
  * Implemented tunable **Proportional–Integral–Derivative (PID)** loop with live-adjustable gains via potentiometers for on-the-fly tuning.
  * Added **threshold-based turn normalization** to prevent motor saturation under varying battery voltage conditions (`if |turn| > 1 → scale by empirically-derived constant`).
  * **Empirically characterized hardware** across battery states — tested fresh vs. depleted conditions to derive optimal scaling constants, compensating for reduced drive authority as voltage dropped.
  * Adaptive logic maintained **consistent high-speed performance** across competition runs despite power fluctuations.

* **Full-System Integration:** Designed both **hardware and firmware**, including schematic wiring, sensor calibration, and driver-level control logic.  

* **⚡ Real-Time Feedback:** Combined multiple photoresistor readings into a weighted average for precise line detection and correction.  

* **Rapid Prototyping:** Iterated quickly using Arduino IDE and modular helper functions for calibration, sensor reading, and error compensation.  

* **System Validation:** Measured motor outputs, response times, and PID stability across varied lighting and surface conditions.

---

## 🛠️ Technical Stack

* **Hardware:**
  * Arduino Mega 2560 (ATmega2560)
  * Dual H-Bridge Motor Driver (L298N)
  * 7-Channel Photoresistor Array
  * Potentiometers for PID Gain Control
  * Battery-Powered Mobile Platform

* **Software:**
  * C/C++ (Arduino Framework)
  * PID Control Algorithm (Tunable Gains + Adaptive Scaling)
  * Modular Calibration and Motor Control Functions
  * Battery-Aware Nonlinear Control Logic

* **Testing & Calibration:**
  * Serial feedback for debugging and gain visualization
  * Manual calibration sequence with LED indicators
  * Real-time tuning via potentiometers during operation
  * Empirical battery characterization for adaptive control

---

## 🚀 Summary
This project showcases a complete **closed-loop embedded control system** — blending analog sensing, real-time computation, hardware characterization, and adaptive nonlinear control.  

Through iterative testing, empirical battery profiling, and dynamic tuning, the robot achieved fast, stable, and accurate line-following performance with robust adaptability across varying power and environmental conditions.

---

## 📄 License
Licensed under the MIT License – see the [LICENSE](LICENSE) file for details.
