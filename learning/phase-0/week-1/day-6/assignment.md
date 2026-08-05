# 🤖 RoboNova

# Phase 0 – Week 1 – Day 6

# Assignment

## Task

Design RoboNova's sensor system for a home environment.

---

## 1. Sensor Placement

| Sensor            | Location            | Purpose                                           |
| ----------------- | ------------------- | ------------------------------------------------- |
| Camera            | Head                | Face recognition, object detection, navigation    |
| Microphone        | Head                | Receive voice commands and communicate with users |
| Ultrasonic Sensor | Front chest         | Measure distance and detect obstacles             |
| Touch Sensors     | Hands and shoulders | Detect physical contact and improve interaction   |

---

## 2. Sensor Workflow

### Scenario

A user says:

**"RoboNova, please bring me my water bottle."**

### Workflow

1. The **microphone** receives the voice command.
2. The **controller** processes and understands the command.
3. The **camera** searches for and identifies the water bottle.
4. The **ultrasonic sensor** detects obstacles and measures the distance to them.
5. The **controller** plans a safe path.
6. The **actuators** move RoboNova toward the bottle.
7. RoboNova picks up the bottle using its robotic arm.
8. The **ultrasonic sensor** continues monitoring for obstacles while returning.
9. RoboNova safely delivers the bottle to the user.

---

## 3. Why Multiple Sensors Are Needed

RoboNova cannot rely on a single sensor because every sensor has a different responsibility. The camera provides vision and object recognition, the microphone receives voice commands, the ultrasonic sensor measures distance and avoids obstacles, and the touch sensor detects physical contact. The controller combines information from all these sensors to make intelligent decisions and perform tasks safely.

---

## 4. Future Improvements

In the future, RoboNova may include additional sensors such as:

* Temperature Sensor
* Gas Sensor
* GPS Module (for outdoor navigation)
* Infrared Sensor
* LIDAR
* IMU (Inertial Measurement Unit)

These sensors will improve RoboNova's intelligence, safety, and navigation capabilities.

---

# Reflection

Today's lesson helped me understand that sensors are the robot's way of perceiving the environment. I learned that no single sensor can perform every task. Instead, multiple sensors work together, and the controller combines their information to make intelligent decisions. This lesson also helped me understand how RoboNova will interact safely with people and its surroundings in a real home environment.
