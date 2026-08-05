# 🤖 RoboNova

# Phase 0 – Week 1 – Day 4

# Robot Degrees of Freedom (DOF), Joints & Links

---

# 1. Degrees of Freedom (DOF)

# Video Resources

## Robot Joints Explained

▶️ Watch:
[Robot Joints and Degrees of Freedom Explained](https://youtu.be/zI64DyaRUvQ?si=OlxhwdyZA0OEVo5T)

## What is DOF?

A **Degree of Freedom (DOF)** is one independent way in which a robot or any object can move.

In simple words:

> **1 DOF = 1 independent movement**

Examples:

* A door opening and closing → 1 DOF
* A robot arm rotating and bending → Multiple DOFs

---

## Why DOF is Important?

Degrees of Freedom determine:

* How flexible a robot is.
* How naturally it can move.
* What tasks it can perform.
* How complex the robot design will be.

More DOFs allow RoboNova to:

* Move in multiple directions.
* Perform complex tasks.
* Interact with objects more naturally.

However, more DOFs do not always mean a better robot because they also increase:

* Mechanical complexity
* Programming difficulty
* Cost
* Power consumption

The goal is to choose the right number of DOFs according to the robot's purpose.

---

# 2. Robot Joints

## What is a Robot Joint?

A robot joint is the connection between two robot parts (links) that allows them to move relative to each other.

Human body comparison:

* Bones → Robot links
* Joints (elbow, knee, shoulder) → Robot joints
* Muscles → Actuators

Joints create movement, and movement creates Degrees of Freedom.

---

# 3. Types of Robot Joints

## 3.1 Revolute Joint 🔄

A revolute joint allows rotational movement around a fixed axis.

### Movement:

* Rotation

### DOF:

* Usually 1 DOF

### Examples:

Human:

* Elbow
* Shoulder
* Wrist

Robot:

* Robotic arm joints

Real-world example:

A door hinge is a revolute joint because the door rotates around a fixed axis.

![Revolute Joint](images/revolute-joint.png)

---

## 3.2 Prismatic Joint ↔️

A prismatic joint allows linear movement along a single axis.

### Movement:

* Sliding
* Extension and contraction

### DOF:

* Usually 1 DOF

### Examples:

* Hydraulic cylinders
* Telescopic robot arms
* Linear actuators

Real-world example:

A drawer is similar to a prismatic joint because it moves forward and backward in a straight line.

![Prismatic Joint](images/prismatic-joint.png)

---

## 3.3 Fixed Joint 🔒

A fixed joint connects two robot parts but does not allow movement.

### Movement:

* No movement

### DOF:

* 0 DOF

Examples:

* Robot frame
* Permanent structural connections

![Fixed Joint](images/fixed-joint.png)

---

# 4. Robot Links

## What is a Robot Link?

A robot link is a rigid part of a robot that connects joints and provides structure.

Simple comparison:

> **Links are robot bones, and joints are the connections that allow movement.**

Example:

RoboNova arm:

```
Shoulder Joint
      |
Upper Arm Link
      |
Elbow Joint
      |
Forearm Link
      |
Wrist Joint
      |
Hand Link
```

![Robot Links and Joints](images/robot-links-joints.png)

---

# 5. Human Body vs Robot Arm

The human body is an inspiration for robot design.

Comparison:

| Human Body | Robot       |
| ---------- | ----------- |
| Bone       | Link        |
| Joint      | Robot Joint |
| Muscle     | Actuator    |
| Brain      | Controller  |

The human elbow is similar to a revolute joint because both provide rotational movement.

![Human vs Robot Arm](images/human-vs-robot-arm.png)

---

# 6. DOF Example in Robot Arm

A robot arm with 3 revolute joints:

* Shoulder → 1 DOF
* Elbow → 1 DOF
* Wrist → 1 DOF

Total:

```
1 + 1 + 1 = 3 DOF
```

More joints can provide more movement flexibility.

![6 DOF Robot Arm](images/6dof-robot-arm.png)

---

# 7. RoboNova Application

For RoboNova:

Possible joint design:

* Shoulder → Revolute Joint
* Elbow → Revolute Joint
* Wrist → Revolute Joint
* Body connections → Fixed Joints

Future designs may include prismatic joints for:

* Arm extension
* Height adjustment
* Special mechanisms

The final number of DOFs will depend on the tasks RoboNova needs to perform.

---

# Key Learning Summary

Today I learned:

* DOF represents independent robot movements.
* Joints create movement and provide DOFs.
* Links provide robot structure.
* Revolute joints create rotation.
* Prismatic joints create linear motion.
* Fixed joints do not allow movement.
* More DOFs increase flexibility but also increase complexity.
* RoboNova's movement design depends on its future tasks.

---

# Engineering Concept

```
Links + Joints + Actuators
            ↓
       Robot Movement
            ↓
          DOF
            ↓
   Robot Capability
```
