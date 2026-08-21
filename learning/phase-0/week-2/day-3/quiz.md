# 🤖 RoboNova — Week 2 → Day 3 Quiz

**Phase:** Phase 0 — Robotics Foundation
**Week:** Week 2 — Electronics & Electricity
**Day:** Day 3
**Topic:** Ohm's Law

---

## 🏆 Final Score

**19 / 20 — 95%**

Excellent performance demonstrating a strong understanding of Ohm's Law and its application to RoboNova's electrical systems.

---

# ❌ Mistake Analysis

## Q4 — Finding Current

### Question

A RoboNova circuit has:

* Voltage = **24 V**
* Resistance = **8 Ω**

What is the current?

### My Answer

**D) 192 A**

### Correct Answer

**B) 3 A**

### What I misunderstood

I multiplied voltage and resistance instead of dividing.

The correct formula for finding current is:

[
I = \frac{V}{R}
]

Therefore:

[
I = \frac{24}{8} = 3A
]

### Key Rule

> **When finding current, divide voltage by resistance.**

---

# 🧠 Concepts Demonstrated Successfully

During the quiz, I correctly understood:

* Voltage and current have a direct relationship when resistance is constant.
* Resistance and current have an inverse relationship when voltage is constant.
* Lower resistance can allow greater current to flow.
* Higher resistance can reduce current.
* Ohm's Law can be rearranged to find any of the three quantities.
* Ohm's Law can be used to analyze RoboNova electrical circuits.
* Electrical problems can be investigated using voltage, current, and resistance.
* Real components must be operated according to their specifications and datasheets.

---

# 📐 Ohm's Law

Ohm's Law describes the relationship between:

* **Voltage (V)**
* **Current (I)**
* **Resistance (R)**

The main formula is:

[
V = I \times R
]

The formula can be rearranged into three forms.

### Find Voltage

[
V = I \times R
]

**Multiply current by resistance.**

### Find Current

[
I = \frac{V}{R}
]

**Divide voltage by resistance.**

### Find Resistance

[
R = \frac{V}{I}
]

**Divide voltage by current.**

---

# 🔑 Formula Selection Rule

| Unknown    | Formula          | Operation |
| ---------- | ---------------- | --------- |
| Voltage    | (V = I \times R) | Multiply  |
| Current    | (I = V/R)        | Divide    |
| Resistance | (R = V/I)        | Divide    |

### Quick Memory Trick

**Finding V → Multiply**

**Finding I → Divide**

**Finding R → Divide**

---

# 🤖 RoboNova Application

Ohm's Law is important in RoboNova because the robot will contain many electrical systems.

A simplified electrical architecture is:

```text
🔋 Battery
     ↓
⚡ Power Distribution
     ↓
🧠 Controller / Motor Driver
     ↓
⚙️ Motors
     ↓
🤖 Movement
```

Ohm's Law helps us reason about:

* Current flowing through circuits
* Electrical resistance
* Motor circuits
* Wiring
* Component requirements
* Power distribution
* Troubleshooting
* Electrical safety

---

# 🔬 Example 1 — Finding Current

Suppose a motor circuit has:

* Voltage = **12 V**
* Resistance = **6 Ω**

Using:

[
I = \frac{V}{R}
]

Substitute the values:

[
I = \frac{12}{6}
]

Therefore:

[
I = 2A
]

### Result

**Current = 2 A**

---

# 🔬 Example 2 — Resistance Increases

If voltage stays constant and resistance increases:

[
R \uparrow \Rightarrow I \downarrow
]

### Relationship

**Resistance ↑ → Current ↓**

---

# 🔬 Example 3 — Resistance Decreases

If voltage stays constant and resistance decreases:

[
R \downarrow \Rightarrow I \uparrow
]

### Relationship

**Resistance ↓ → Current ↑**

---

# 📚 Topics to Review

Only one main area needs additional practice:

## 1. Choosing the Correct Ohm's Law Formula

Especially remember:

[
I = \frac{V}{R}
]

when calculating current.

## 2. Distinguishing Between Multiplication and Division

| Quantity to Find | Operation |
| ---------------- | --------- |
| Voltage          | Multiply  |
| Current          | Divide    |
| Resistance       | Divide    |

---

# 🎓 Lessons Learned

* Ohm's Law connects voltage, current, and resistance.
* Voltage represents electrical potential difference.
* Current represents the flow of electrical charge.
* Resistance opposes current flow.
* When resistance is constant, increasing voltage increases current.
* When voltage is constant, increasing resistance decreases current.
* Ohm's Law can be rearranged depending on the unknown quantity.
* Electrical calculations can help engineers troubleshoot real hardware.
* RoboNova's electrical system must be designed using real component specifications.
* Mathematical understanding should be combined with datasheets and engineering safety limits.

---

# 🪞 Self-Reflection

Today's quiz strengthened my understanding of Ohm's Law and how voltage, current, and resistance interact.

I correctly solved most conceptual and calculation-based questions and applied the relationships to RoboNova's electrical system.

My main mistake was choosing multiplication instead of division when calculating current in one question. I understand the correction and need to continue practicing the three rearranged forms of Ohm's Law so that I can select the correct formula quickly.

The most useful part of today's lesson was connecting mathematical relationships to real engineering problems such as motor behavior, wiring resistance, and electrical troubleshooting.

---

# 🌟 Extra Practice MCQs

The following questions are additional learning material for anyone visiting the RoboNova repository and wanting to practice basic robotics electronics.

---

## Q21

A circuit has **10 V** and **5 Ω** resistance. What is the current?

A) 0.5 A
B) 2 A
C) 5 A
D) 50 A

---

## Q22

A circuit has **3 A** of current and **4 Ω** resistance. What is the voltage?

A) 0.75 V
B) 7 V
C) 12 V
D) 16 V

---

## Q23

A circuit operates at **20 V** and draws **4 A**. What is the resistance?

A) 0.2 Ω
B) 5 Ω
C) 16 Ω
D) 80 Ω

---

## Q24

If voltage remains constant and resistance is doubled, what happens to current?

A) Current doubles
B) Current becomes half
C) Current remains unchanged
D) Current becomes zero

---

## Q25

Which quantity is measured in Ohms (Ω)?

A) Voltage
B) Current
C) Resistance
D) Power

---

## Q26

A RoboNova motor circuit has constant voltage. The resistance decreases significantly. What is the expected effect?

A) Current decreases
B) Current increases
C) Voltage becomes zero
D) Resistance increases automatically

---

## Q27

Which formula calculates current?

A) (I = V \times R)
B) (I = V/R)
C) (I = R/V)
D) (I = V + R)

---

## Q28

Why is Ohm's Law useful in robotics?

A) It determines robot personality
B) It helps analyze and troubleshoot electrical circuits
C) It replaces the robot controller
D) It controls mechanical joints directly

---

## Q29 — True or False

If resistance is constant, doubling the voltage doubles the current.

**Answer:** True / False

---

## Q30 — True or False

If voltage is constant, increasing resistance generally decreases current.

**Answer:** True / False

---

# 🧠 Visitor Learning Challenge

Try solving the extra questions before checking a calculator or textbook.

Recommended engineering workflow:

```text
Identify Known Values
        ↓
Identify Unknown
        ↓
Choose Ohm's Law Formula
        ↓
Substitute Values
        ↓
Calculate
        ↓
Check Units
        ↓
Interpret the Result
```

This is the same basic engineering reasoning used throughout RoboNova.

---

# 📈 Day 3 Quiz Summary

| Category            | Result                        |
| ------------------- | ----------------------------- |
| Total Questions     | 20                            |
| Correct             | 19                            |
| Incorrect           | 1                             |
| Final Score         | **95%**                       |
| Understanding       | **Excellent**                 |
| Main Weakness       | Formula selection for current |
| Overall Performance | 🏆 Excellent                  |

---

# 🎯 Day 3 Key Takeaway

The most important formula to remember from today's lesson is:

[
\boxed{I = \frac{V}{R}}
]

**Voltage ÷ Resistance = Current**

And the complete Ohm's Law relationship is:

[
\boxed{V = I \times R}
]

```text
       V
      ---
      I R
```

Understanding these relationships will become important when RoboNova moves from basic electrical theory toward real components, motors, controllers, and power systems.

---

## 🤖 RoboNova Progress

**Phase 0 — Robotics Foundation**

**Week 2 — Electronics & Electricity**

* ✅ Day 1 — Electricity Fundamentals
* ✅ Day 2 — Electrical Components & Circuits
* ✅ Day 3 — Ohm's Law
* ⬜ Day 4 — Next Topic

**Day 3 Status: COMPLETED 🏆**

**Score: 19/20 — 95%**
