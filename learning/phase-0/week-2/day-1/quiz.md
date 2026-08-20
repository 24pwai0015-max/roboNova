# 🤖 RoboNova

# Phase 0 – Week 2 – Day 8

# Quiz

## Topic: Introduction to Electronics & Electricity

**Quiz Score: 64/65 — 98.5% 🏆**

---

# Part 1 — Multiple Choice Questions

### Q1. What is the primary source of electrical energy in RoboNova?

A. Sensor
B. Battery
C. Controller
D. Motor

**Your Answer:** B
**Result:** ✅ Correct

---

### Q2. What is the main purpose of wires?

A. Make decisions
B. Detect obstacles
C. Provide a conductive path
D. Produce mechanical movement

**Your Answer:** C
**Result:** ✅ Correct

---

### Q3. What happens when a circuit is broken?

A. Current flows normally
B. Current cannot flow through the complete path
C. The motor becomes faster
D. The battery produces more energy

**Your Answer:** B
**Result:** ✅ Correct

---

### Q4. A camera sends information to the controller. This information is primarily:

A. Mechanical energy
B. Electrical energy
C. An electrical signal
D. Battery power

**Your Answer:** C
**Result:** ✅ Correct

---

### Q5. What is the main role of the controller?

A. Store electrical energy
B. Process information and make decisions
C. Produce mechanical movement
D. Distribute battery power

**Your Answer:** B
**Result:** ✅ Correct

---

### Q6. Why does RoboNova use a motor driver?

A. To detect people
B. To store sensor data
C. To interface the controller with higher-power motors
D. To replace the battery

**Your Answer:** C
**Result:** ✅ Correct

---

### Q7. Which represents information flow?

A. Battery → Motor
B. Battery → Power Distribution
C. Sensor → Controller
D. Battery → Motor Driver

**Your Answer:** C
**Result:** ✅ Correct

---

### Q8. Which represents power flow?

A. Sensor → Controller
B. Battery → Power Distribution → Components
C. Camera → Controller
D. Controller → Motor Driver

**Your Answer:** B
**Result:** ✅ Correct

---

### Q9. Which component converts electrical energy into mechanical movement?

A. Battery
B. Motor
C. Sensor
D. Wire

**Your Answer:** B
**Result:** ✅ Correct

---

### Q10. Which statement best describes robotics?

A. Robotics is only electronics
B. Robotics is only programming
C. Robotics combines electronics, mechanics, software, sensing, and control
D. Robotics is only motors

**Your Answer:** C
**Result:** ✅ Correct

### Part 1 Score: **10/10** 🎯

---

# Part 2 — True / False

### Q11. A battery provides electrical energy to RoboNova.

**Your Answer:** True
**Result:** ✅ Correct

---

### Q12. An electrical signal can carry information from a sensor to a controller.

**Your Answer:** True
**Result:** ✅ Correct

---

### Q13. Power flow and information flow are exactly the same thing.

**Your Answer:** False
**Result:** ✅ Correct

---

### Q14. A motor driver can receive a control signal from the controller and use power from the power system to operate a motor.

**Your Answer:** True
**Result:** ✅ Correct

---

### Q15. A broken electrical connection can prevent a component from operating.

**Your Answer:** True
**Result:** ✅ Correct

### Part 2 Score: **5/5** 🎯

---

# Part 3 — Scenario-Based Questions

## Q16 — Obstacle Detection

**Scenario:**

RoboNova is moving forward. Its ultrasonic sensor detects a chair.

Explain what happens from:

**Ultrasonic Sensor → Controller → Decision → Motor Driver → Motor → Movement**

### Your Answer

The ultrasonic sensor detects the obstacle. The controller receives this signal, processes it, and makes a proper decision. It sends a control signal to the motor driver. The motor driver forwards the control signal to the motors and actuators.

There is also electrical energy involved because all these components need power to operate.

### Evaluation

**10/10 — Correct ✅**

You correctly explained both:

* 📡 Information flow
* ⚡ Power flow

### Technical refinement

The controller sends a control signal to the motor driver. The motor driver then uses electrical power from the power system to drive the motor.

---

# Q17 — Empty Battery

**Scenario:**

RoboNova's sensors, Arduino, Raspberry Pi, motors, and wires are all properly connected, but the battery is completely empty.

### Your Answer

No, because the battery is empty and it is the power house.

### Evaluation

**10/10 — Correct ✅**

The battery is RoboNova's electrical energy source. Without available electrical energy, the components cannot operate normally.

---

# Q18 — Broken Circuit

**Scenario:**

RoboNova's battery is fully charged, but one important wire in the motor circuit is broken.

### Your Answer

The current will not flow because current flows in a closed circuit. There is no energy to the components, so it will not work properly and will not communicate with each other.

### Evaluation

**9/10 — Mostly Correct ✅**

You correctly understood that:

* The circuit is broken.
* The complete current path is interrupted.
* The motor cannot operate normally.

### Correction

The statement **"there is no energy to the components"** is too broad.

The battery still contains energy, and other components may still have power if they are connected through separate intact circuits.

Also, a broken motor-power wire does not necessarily stop communication between all components.

### Better understanding

> A broken wire interrupts the motor's electrical path, so the motor cannot receive the required electrical power through that circuit and cannot operate normally.

---

# Q19 — Power vs Information

**Scenario:**

The ultrasonic sensor needs electrical energy to operate and sends distance information to the controller.

### Your Answer

The electrical energy comes from the battery, and the information is carried by an electrical signal.

### Evaluation

**10/10 — Correct ✅**

Correct distinction:

**🔋 Battery → Electrical Energy → Sensor**

**📡 Sensor → Electrical Signal → Controller**

---

# Q20 — Complete RoboNova Task

**Scenario:**

RoboNova receives the command:

> "Bring me a water bottle."

Explain the role of:

**Battery → Sensors → Controller → Motor Driver → Motors**

### Your Answer

The battery provides energy to the sensors.

The microphone listens to the voice command.

The camera navigates the water bottle.

The ultrasonic sensor clears the path and measures distance.

All this information goes to the controller through electrical signals. The controller processes the information, makes a decision, and sends a control signal to the motor driver. Then the signal goes to the motors.

This is information flow. All these processes work because the components receive power from the battery, including the sensors, controllers, motor driver, and motors.

### Evaluation

**10/10 — Correct ✅**

You successfully combined **power flow and information flow**.

### Technical refinement

Instead of saying:

> "The camera navigates the water bottle."

Use:

> **The camera provides visual information that helps the controller locate and identify the water bottle and understand the surroundings.**

The camera is the **sensor**. Navigation and decision-making are performed by the controller/software using sensor information.

---

# 📊 Final Results

| Section            |     Score |
| ------------------ | --------: |
| MCQs               | **10/10** |
| True / False       |   **5/5** |
| Scenario Questions | **49/50** |
| **TOTAL**          | **64/65** |

# 🏆 Final Score: 98.5%

## Performance: Excellent

### What I Understand Well

* ⚡ Electrical energy
* 🔋 Battery
* 🔌 Electrical circuits
* 📡 Electrical signals
* 🔄 Power flow
* 📡 Information flow
* 🧠 Controller
* 🎛️ Motor driver
* ⚙️ Motor operation
* 🤖 Sense → Think → Act relationship
* 🔋 Power + information working together

### Minor Areas to Improve

1. Distinguish **power supply** from **communication signals** more precisely.
2. Remember that a **camera provides information**; the controller/software performs navigation and decision-making.
3. A broken wire in one circuit does not necessarily mean **all RoboNova components lose power or communication**.

---

# 🧠 Day 8 Core Concept

The most important concept from today's lesson:

> **RoboNova needs both POWER FLOW and INFORMATION FLOW.**

### ⚡ Power Flow

**Battery → Power Distribution → Components**

### 📡 Information Flow

**Sensors → Controller → Control Signal → Motor Driver → Motors**

Together, these allow RoboNova to:

**Sense → Think → Act** 🤖
