# 🤖 RoboNova

# Phase 0 – Week 1 – Day 7

# Notes

# Topic: Week 1 Review

## Introduction

This day was dedicated to reviewing everything learned during Week 1. Instead of studying a new topic, I connected all the concepts together to understand how RoboNova works as a complete robotic system.

---

# Week 1 Topics

## Day 1

* Introduction to Robotics
* Sense → Think → Act cycle

## Day 2

* Robot Architecture
* Mechanical Body
* Sensors
* Controller
* Actuators
* Power Supply
* Communication

## Day 3

* Types of Robots
* Industrial Robot
* Service Robot
* Mobile Robot
* Humanoid Robot
* Autonomous Robot
* Collaborative Robot (Cobot)

## Day 4

* Degrees of Freedom (DOF)
* Robot Joints
* Revolute Joint
* Prismatic Joint
* Fixed Joint

## Day 5

* Robot Movement
* Wheels and Legs
* Locomotion
* Movement Planning

## Day 6

* Camera
* Microphone
* Ultrasonic Sensor
* Touch Sensor
* Sensor Fusion (Introduction)

---

# RoboNova Summary

## Robot Type

* Humanoid Robot
* Service Robot
* Mobile Robot

---

## Main Components

### Sensors

* Camera
* Microphone
* Ultrasonic Sensor
* Touch Sensor

### Controller

* Raspberry Pi
* Arduino Uno

### Actuators

* Servo Motors
* DC Motors
* Stepper Motors

### Mechanical Body

* 3D Printed Plastic Chassis

### Power Supply

* Li-ion Battery

### Communication

* Wi-Fi
* Bluetooth
* Mobile Application

---

# Sense → Think → Act

```text
Environment
      ↓
Sensors
      ↓
Controller
      ↓
Decision
      ↓
Actuators
      ↓
Action
```

---

# RoboNova Workflow Example

User Command:

"Bring me a water bottle."

Workflow:

1. The microphone receives the voice command.
2. The controller understands the command.
3. The camera searches for and identifies the water bottle.
4. The ultrasonic sensor detects obstacles and measures distance.
5. The controller plans the safest route.
6. The actuators move RoboNova toward the bottle.
7. RoboNova picks up the bottle.
8. The ultrasonic sensor continues monitoring while returning.
9. RoboNova safely delivers the bottle to the user.

---

# Key Learnings

* A robot is a complete system made of multiple components.
* Every sensor has a specific responsibility.
* The controller combines sensor information before making decisions.
* Actuators convert controller commands into movement.
* Multiple sensors working together produce better decisions than a single sensor.
* RoboNova is being designed as a humanoid service robot for household assistance.

---

# Week 1 Reflection

Week 1 gave me a strong foundation in robotics. I learned the basic components of a robot, different robot types, movement, joints, sensors, and how all these parts work together. I now understand RoboNova as a complete robotic system rather than a collection of separate components. This knowledge will help me build the hardware and software in the coming weeks.
