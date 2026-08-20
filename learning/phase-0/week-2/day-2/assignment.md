# RoboNova — Phase 0 – Week 2 – Day 9
## Assignment: Voltage, Current, Resistance, Power & Electrical Architecture

**Topic:** Electrical Fundamentals applied to RoboNova  
**Goal:** Understand the four basic electrical quantities and how they work together in RoboNova’s power system.

---

### Part 1 — The Four Basic Electrical Quantities

**Q1. What is Voltage?**  
**Answer:**  
Voltage is the electrical “push” or pressure that forces electric charge to move through a circuit.  
It is the difference in electric potential between two points.  

Symbol: **V**  
Unit: **Volt (V)**  

In RoboNova, the battery provides the voltage that pushes current through every component.

---

**Q2. What is Current?**  
**Answer:**  
Current is the flow of electric charge through a conductor.  
It is the rate at which charge moves past a point in the circuit.  

Symbol: **I**  
Unit: **Ampere (A)**  

In RoboNova, current is what actually delivers energy to sensors, controllers, motor drivers and motors.

---

**Q3. What is Resistance?**  
**Answer:**  
Resistance is the opposition that a material or component offers to the flow of current.  
Higher resistance means less current can flow for a given voltage.  

Symbol: **R**  
Unit: **Ohm (Ω)**  

Every wire, connector, sensor and motor in RoboNova has some resistance.

---

**Q4. What is Electrical Power?**  
**Answer:**  
Electrical power is the rate at which electrical energy is transferred or converted.  

Formula:

```
P = V × I
```

Where:  
- **P** = power  
- **V** = voltage  
- **I** = current  

The unit of power is the **watt (W)**.

---

### Part 2 — Ohm’s Law

**Q5. Write Ohm’s Law and explain its variables.**  
**Answer:**  

```
V = I × R
```

Where:  
- **V** = voltage (volts)  
- **I** = current (amperes)  
- **R** = resistance (ohms)  

It describes the fundamental relationship between voltage, current and resistance.  

When voltage is constant:  
- Higher resistance → lower current  
- Lower resistance → higher current  

---

**Q6. Calculate the current.**  
A RoboNova component operates at **12 V** and has a resistance of **6 Ω**.  
Calculate the current.  

Use Ohm’s Law rearranged:

```
I = V / R
```

**My calculation:**

```
I = 12 V / 6 Ω = 2 A
```

**Answer:** **2 A**

---

### Part 3 — Electrical Power

**Q7. Calculate electrical power.**  
A RoboNova component operates at **5 V** and draws **2 A**.  
Calculate its electrical power.  

Use:

```
P = V × I
```

**My calculation:**

```
P = 5 V × 2 A = 10 W
```

**Answer:** **10 W**

---

### Part 4 — Voltage Requirements

**Q8. Why can’t the battery’s voltage simply be connected directly to every RoboNova component?**  
**Answer:**  
We cannot apply the battery voltage directly to every component because different components have different voltage requirements and allowable voltage ranges.  

If a component receives excessive voltage, it may:  
- Overheat  
- Malfunction  
- Become permanently damaged  
- Fail completely  

Therefore, RoboNova requires appropriate **power distribution** and **voltage regulation** so that each component receives only the voltage it is designed for (for example 5 V for Arduino, 5 V or 3.3 V for sensors, higher voltage for motors).

---

### Part 5 — Power Distribution

**Q9. Explain RoboNova’s power distribution system.**  
**Answer:**  
RoboNova’s battery acts as the main electrical energy source.  
The electrical energy passes through protection devices (fuse / switch) and power-distribution components before reaching the different subsystems.  

A simplified architecture is:

```
Battery
   ↓
Main Switch / Fuse / Protection
   ↓
Power Distribution Board
   ├── Voltage Regulator → Raspberry Pi
   ├── Voltage Regulator → Arduino
   ├── Voltage Regulator → Sensors
   └── Motor Driver ← higher current path → Motors
```

Different branches can supply:  
- Raspberry Pi  
- Arduino  
- Sensors  
- Motor driver  
- Motors  

The actual voltage and current requirements must always be verified from the component datasheets.

---

### Part 6 — Motor vs Sensor

**Q10. Why can motors require more current than small sensors?**  
**Answer:**  
Motors convert electrical energy into mechanical movement.  
Because mechanical movement requires significant energy, motors can require substantially greater current than small electronic sensors.  

Motors may draw especially high current during:  
- Startup  
- Acceleration  
- High mechanical load  
- High-torque operation  
- Stall conditions  

Sensors generally have much lower power requirements because their primary purpose is sensing and generating small electrical signals, not producing mechanical work.  

However, the exact current depends on the specific component and its operating conditions.

---

### Part 7 — Motor Driver

**Q11. What is the role of a motor driver in RoboNova?**  
**Answer:**  
The motor driver provides the interface between the low-power controller and the high-power motor system.  

```
Controller (low-power signal)
        ↓
   Motor Driver
        ↓
Motors (high current)
```

The controller sends a low-power control signal (PWM, direction, enable) to the motor driver.  
The motor driver then switches and controls the much higher current required by the motors.  

This protects the controller from the high currents that motors need and allows precise control of speed and direction.

---

### Part 8 — Power Flow vs Information Flow

**Q12. Explain the difference between power flow and information flow in RoboNova.**  
**Answer:**  

**Power Flow**

```
Battery → Power Distribution → Components (energy supply)
```

Power flow provides the electrical energy required for components to operate.

**Information Flow**

```
Sensors → Controller → Decision → Motor Driver → Motors → Movement
```

Information flow carries sensor data and control commands.

**Main difference:**  
Power makes the components operate.  
Information allows RoboNova to sense, think and act intelligently.  

Both are required for RoboNova to function properly.

---

### Part 9 — Electrical Troubleshooting

**Q13. RoboNova’s motors are moving weakly, but the Raspberry Pi is working. What electrical areas should be checked?**  
**Answer:**  
I would investigate the motor power path specifically:

```
Battery → Fuse/Switch → Power Distribution → Motor Driver → Motors
```

Possible causes include:  
1. Battery voltage is too low.  
2. Battery cannot provide enough current under load.  
3. Significant voltage drop when motors start.  
4. Problem in the power distribution path for the motors.  
5. A wire or connector has excessive resistance.  
6. Motor driver is not receiving sufficient power.  
7. Motor driver cannot supply enough current.  
8. Motors are overloaded or partially damaged.  

The fact that the Raspberry Pi is working only proves that its own (usually lower-current) power path is healthy. It does **not** prove that the high-current motor power system is healthy.

---

### Part 10 — Engineering Thinking

**Q14. Why is checking the electrical architecture important before replacing components?**  
**Answer:**  
Because the problem may not be caused by the component itself.  

For example, a weak motor could be caused by:  
- Low battery voltage  
- Insufficient current capability  
- Voltage drop under load  
- High resistance in wires or connectors  
- Poor connection  
- Faulty motor driver  
- Incorrect power distribution  

Checking the electrical architecture first helps identify the real source of the problem and prevents unnecessary replacement of good components.

---

### Part 11 — RoboNova Electrical Architecture

**Q15. Design a simplified electrical architecture for RoboNova.**  

**My Architecture:**

```
🔋 Li-ion Battery
        │
        ↓
   Main Switch + Fuse (Protection)
        │
        ↓
🔌 Power Distribution Board
        │
   ┌────┼────────────────┬────────────────┐
   │    │                │                │
   ↓    ↓                ↓                ↓
Voltage  Voltage      Voltage         High-Current
Regulator Regulator   Regulator       Path
(5 V)    (5 V / 3.3 V) (5 V)         
   │        │             │               │
   ↓        ↓             ↓               ↓
Raspberry  Sensors     Arduino        Motor Driver
Pi         (Camera,                   (receives control
           Ultrasonic,                 signals from
           Mic, Touch)                 Arduino / Pi)
                                          │
                                          ↓
                                       ⚙️ Motors
```

**Explanation:**  
- The battery provides the main electrical energy.  
- Protection (switch + fuse) controls and safeguards the supply.  
- The power-distribution system routes energy to the different subsystems.  
- Voltage regulators provide the correct voltage levels for logic and sensors.  
- The motor driver sits on a higher-current path and is controlled by the low-power controllers.

---

### Part 12 — Reflection

**Q16. What is the most important concept I learned today?**  
**Answer:**  
The most important concept is that voltage, current, resistance and power are four different but tightly related electrical quantities. Together they completely determine how RoboNova’s electrical system behaves.

**Q17. What was the most difficult concept?**  
**Answer:**  
The difference between voltage and current was initially confusing.  
I understood it better with the simple analogy:  
- **Voltage = the push**  
- **Current = the flow**

**Q18. How will this knowledge help me build RoboNova?**  
**Answer:**  
This knowledge will help me:  
- Select appropriate batteries and power supplies  
- Understand voltage and current requirements of every component  
- Use voltage regulators correctly  
- Design a safe and reliable power distribution system  
- Choose suitable motor drivers  
- Troubleshoot electrical problems systematically  
- Avoid applying incorrect voltage to sensitive components  
- Understand why motors need much higher current capability than sensors

---

### 🧠 Final Day 9 Summary

**Key electrical concepts:**

```
Voltage (V)   → the push
Current (I)   → the flow
Resistance (R) → the opposition
Power (P)     → the rate of energy use  (P = V × I)
Ohm’s Law     → V = I × R
```

**For RoboNova:**

```
Battery → Protection → Power Distribution → Voltage Regulation → Components
                                                      ↓
                                               Motor Driver → Motors
```

The electrical system supplies the energy that every component needs to operate.  
The information system allows those components to work together intelligently.  
Both systems must be designed and understood correctly for a reliable robot.

---

### ✅ Assignment Completion Checklist

- [x] Explain voltage  
- [x] Explain current  
- [x] Explain resistance  
- [x] Explain electrical power  
- [x] Explain Ohm’s Law  
- [x] Solve an Ohm’s Law problem  
- [x] Solve a power problem  
- [x] Explain voltage requirements  
- [x] Explain power distribution  
- [x] Explain motor vs sensor current demand  
- [x] Explain motor driver  
- [x] Explain power flow vs information flow  
- [x] Explain electrical troubleshooting  
- [x] Design RoboNova electrical architecture  
- [x] Complete reflection  

**Status:** Assignment complete and ready for submission.  
