# 🤖 RoboNova

# Phase 0 – Week 2 – Day 8

# Assignment

## Topic: Electrical Energy, Circuits, Power Flow & Information Flow

---

# Part 1 — Explain RoboNova's Electrical System

### Q1.

RoboNova cannot operate without electrical energy because every active part of the robot needs a continuous supply of electricity to function.

* The **battery** stores chemical energy and converts it into electrical energy that powers the system.
* **Wires** form conductive paths that carry electrical energy between components.
* **Power distribution** takes the battery supply and distributes or regulates it as required by different components.
* **Sensors** need electrical energy to operate and generate information such as distance, sound, images, and touch.
* The **controllers** (Raspberry Pi + Arduino) need electrical energy to run their processors, memory, and programs.
* The **motor driver** needs power to operate its electronics and control the higher-current supply to the motors.
* **Motors** convert electrical energy into mechanical movement.

If an important link in the electrical system is missing, the corresponding component or subsystem may stop working.

---

# Part 2 — Power Flow

### Q2.

```text
Li-ion Battery
       ↓
Power Distribution
(voltage regulation / power board)
       ↓
   ┌───┼────────┬──────────┐
   ↓   ↓        ↓          ↓
Sensors Arduino Raspberry Motor
        Uno     Pi       Driver
                            ↓
                          Motors
```

Electrical energy leaves the battery and is distributed through the power system to the components that require it.

The sensors, Arduino, Raspberry Pi, and motor driver receive the appropriate electrical supply. The motor driver then uses electrical power from the power system to drive the motors according to the controller's commands.

The motors usually require much more current than logic-level electronics, which is why the motor driver is used between the controller and motors.

---

# Part 3 — Information Flow

### Q3.

```text
Sensors
(Camera, Ultrasonic, Microphone, Touch)
       ↓
  Sensor Data / Signals
       ↓
Controller
(Raspberry Pi + Arduino)
       ↓
Processing & Decision
       ↓
 Control Signal
       ↓
Motor Driver
       ↓
Motors
       ↓
Movement
```

Sensors detect physical information from the environment and convert it into electrical signals or digital data.

The controllers receive this information, process it, run the required software, and make decisions.

The controller sends a control signal to the motor driver. The motor driver uses the available electrical power to control the motors.

The motors then produce mechanical movement.

---

# Part 4 — Power vs Information

### Q4.

| Feature          | Power Flow                                    | Information Flow                                          |
| ---------------- | --------------------------------------------- | --------------------------------------------------------- |
| Purpose          | Supply energy so components can operate       | Carry information so the robot can sense, decide, and act |
| Source           | Battery / power system                        | Sensors and controllers                                   |
| Example          | Battery → Power Distribution → Components     | Ultrasonic → Controller → Motor Driver                    |
| Destination      | Sensors, controllers, motor driver, motors    | Controller → Motor Driver → Motors                        |
| RoboNova example | Battery → Power Board → Motor Driver → Motors | Ultrasonic → Arduino → Controller → Motor Driver          |

### Key Difference

> **Electrical energy powers components, while electrical signals/data carry information and control commands.**

---

# Part 5 — Broken Circuit

### Q5.

1. The motor stops turning, or cannot start normally, because the electrical path to the motor is interrupted.

2. A disconnected wire creates an open circuit. Current requires a complete conductive path through the circuit.

3. No. Only the affected motor circuit necessarily stops working. Sensors, controllers, or other motors connected through separate intact circuits may continue operating.

4. I would check:

   * Battery voltage
   * Motor power wires
   * Motor signal/control wires
   * Connectors
   * Motor-driver power
   * Motor-driver commands
   * Continuity using a multimeter

---

# Part 6 — RoboNova Scenario

### Q6.

RoboNova receives the command:

> **"Bring me a water bottle."**

## Input

* The **microphone** receives the user's voice command.
* The **camera** provides visual information to help locate and identify the water bottle and understand the surroundings.
* The **ultrasonic sensor** detects obstacles and measures distance.
* The **touch sensor**, if used, can detect physical contact such as contact with the bottle or gripper interaction.

All of these sensors require electrical energy to operate.

## Processing

The **Raspberry Pi** can handle higher-level tasks such as speech recognition, computer vision, and navigation/planning.

The **Arduino** can handle real-time low-level tasks such as reading sensors and controlling actuators.

The controllers process the sensor information and determine actions such as:

**Locate bottle → Navigate → Avoid obstacles → Approach → Grasp → Return**

Both controllers require electrical energy to operate.

## Output

The controllers send control signals to the motor driver.

The motor driver uses electrical power from the power system to control the motors.

The motors produce mechanical movement that allows RoboNova to move toward the bottle, grasp it, and return it to the user.

Electrical energy is required throughout the process to operate the sensors, controllers, motor driver, and motors.

---

# Part 7 — Design Your Own RoboNova Electrical Architecture

### Q7.

```text
                 ⚡ POWER FLOW

                  🔋 Li-ion Battery
                         │
                         ↓
                 🔌 Power Distribution
                         │
          ┌──────────────┼───────────────┐
          ↓              ↓               ↓
       Sensors       Controllers      Motor Driver
          │          /          \          │
          │     Arduino       Raspberry   │
          │        Uno            Pi       │
          │                              ↓
          │                           ⚙️ Motors
          │                              ↓
          │                           Movement
          │
          │
          └──────── 📡 INFORMATION FLOW ────────┐
                                                 ↓
                                  🧠 Controller
                                                 ↓
                                          Control Signal
                                                 ↓
                                          🎛️ Motor Driver
                                                 ↓
                                               Motors
```

### Sensors

* 📷 Camera
* 📡 Ultrasonic sensor
* 🎤 Microphone
* 👆 Touch sensor

### Power Flow

**Battery → Power Distribution → Sensors / Controllers / Motor Driver**

The motor driver then uses the available motor power to drive the motors.

### Information Flow

**Sensors → Controller → Decision → Motor Driver → Motors**

The power flow provides the energy required for the components to operate, while the information flow carries sensor data and control commands.

---

# Part 8 — Engineering Thinking

### Q8.

Possible causes if the ultrasonic sensor is working but the controller receives no distance information:

1. The signal/data wire between the sensor and controller may be disconnected or loose.
2. The sensor may have power, but the ground connection between the sensor and controller may be missing.
3. The Arduino may have the wrong pin assignment.
4. The program may contain an incorrect pin configuration or reading method.
5. A connector or signal wire may be damaged.
6. There may be a voltage-level compatibility problem.
7. The controller may not be correctly processing the sensor signal.

The problem should be investigated systematically rather than immediately assuming that the sensor is broken.

---

# Part 9 — Reflection

### Q9.1 — What was the most important concept you learned today?

The most important concept was understanding **power flow and information flow** as two separate but cooperating systems inside RoboNova.

Power flow keeps the components operating, while information flow allows RoboNova to sense, process information, make decisions, and act.

---

### Q9.2 — What is the difference between electrical energy and an electrical signal?

Electrical energy provides the power required for a component to operate.

An electrical signal carries information such as sensor readings or control commands.

---

### Q9.3 — Why does RoboNova need both power flow and information flow?

Power flow allows the robot's components to operate, while information flow allows the robot to work accurately and intelligently.

Without power, the components cannot operate.

Without information, RoboNova cannot properly sense, process, decide, and control its actions.

---

### Q9.4 — Which part of today's lesson was most difficult for you?

The most difficult part was understanding the **motor-driver stage**, especially how the controller sends a low-power control signal while the motor driver uses higher electrical power to operate the motors.

---

### Q9.5 — How does today's electronics knowledge help you build RoboNova in the future?

It helps me understand how **power and information flow through RoboNova**.

This knowledge will help me understand how to connect components, design the electrical architecture, and troubleshoot problems when a component does not work.

---

# 📊 Assignment Evaluation

| Part                         |      Score |
| ---------------------------- | ---------: |
| Q1 — Electrical System       |      10/10 |
| Q2 — Power Flow              |       9/10 |
| Q3 — Information Flow        |      10/10 |
| Q4 — Power vs Information    |      10/10 |
| Q5 — Broken Circuit          |      10/10 |
| Q6 — RoboNova Scenario       |      14/15 |
| Q7 — Electrical Architecture |      11/15 |
| Q8 — Engineering Thinking    |      10/10 |
| Q9 — Reflection              |       6/10 |
| **Original Score**           | **90/100** |

### Finalized After Corrections

The corrections above improve the technical accuracy of the assignment, especially:

* Motor driver and motor power relationship
* Camera vs navigation responsibility
* Clear separation of power and information flow
* Reflection answers

**Final Day 8 Assignment: 90/100 — Excellent 🏆**

---

# 🧠 Day 8 Main Lesson

> **Power makes RoboNova's components operate; information allows RoboNova to sense, think, decide, and act.**

### ⚡ Power Flow

**Battery → Power Distribution → Components**

### 📡 Information Flow

**Sensors → Controller → Decision → Motor Driver → Motors**

### 🤖 Robotics Flow

**Sense → Think → Act**
