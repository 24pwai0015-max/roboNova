# 🤖 RoboNova

# Phase 0 – Week 1 – Day 4

# Assignment

## Task

Design the basic joint system for RoboNova.

Your design should identify:

* The types of joints RoboNova will use.
* Where each joint will be placed.
* An estimated number of Degrees of Freedom (DOFs) for the robotic arm.
* A brief explanation of why these joints were selected.

---

# RoboNova Joint Design

## 1. Revolute Joints

Revolute joints will be used in:

* Shoulder
* Elbow
* Wrist

These joints provide rotational movement, allowing RoboNova to move its arm naturally while reaching, lifting, and manipulating objects.

---

## 2. Prismatic Joints

Prismatic joints may be added in future versions if RoboNova requires:

* Arm extension
* Height adjustment
* Linear movement mechanisms

At the current stage, they are not essential for the basic design.

---

## 3. Fixed Joints

Fixed joints will be used in structural areas where movement is unnecessary, providing stability and strength to the robot's body.

---

# Estimated Degrees of Freedom

For the first version of RoboNova's robotic arm:

* Shoulder → 1 DOF
* Elbow → 1 DOF
* Wrist → 1–2 DOFs

**Estimated Total:** **3–4 DOFs**

This provides sufficient flexibility for basic household tasks such as reaching, picking up, and placing objects.

---

# Design Rationale

The selected joints provide a balance between functionality and simplicity.

* Revolute joints create smooth and natural arm movements.
* Fixed joints improve structural stability.
* Keeping the arm at approximately 3–4 DOFs reduces mechanical complexity, programming effort, power consumption, and overall cost while still allowing RoboNova to perform useful everyday tasks.

---

# Reflection

Through this assignment, I learned that selecting robot joints is an important engineering decision. The number and type of joints directly affect the robot's movement, complexity, cost, and capabilities. Instead of maximizing the number of DOFs, the goal is to choose the optimal design based on the tasks RoboNova is expected to perform.
