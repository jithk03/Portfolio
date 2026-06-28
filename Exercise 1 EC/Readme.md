# Exercise 1: Electrical Circuits
# Date : 30/04/2026
### Digital Design & Fabrication — Portfolio Entry
> Carl von Ossietzky Universität Oldenburg

---

## Overview

In this exercise, we built and tested five electrical circuits across two tasks. Each task started with a base circuit that we progressively modified. We recorded measurements and photos throughout for this portfolio.

---

## Task 1 – LED Control Circuit

**Components:** Resistors (100 Ω, 220 Ω, 1.0 kΩ, 4.7 kΩ), Green LED, 1 kΩ potentiometer, 2-position switch, Breadboard, Jumper wires

---

### Task 1.1 – Simple LED Circuit

We built a series circuit with Vcc = 5V, a current-limiting resistor R1, and a green LED. We measured V1 (across R1) and V_LED using a multimeter, then repeated with different resistor values.

| R1 [Ω] | Measured V1 [V] | Measured V_LED [V] |
|--------|-----------------|--------------------|
| 220    |       2.25      |        2.73        |
| 1000   |       2.18      |        2.74        |
| 4700   |       2.73      |        2.28        |

**Observations:** The voltage across the LED (V_LED) stayed roughly constant regardless of R1 — the LED maintains its forward voltage (~2V). As R1 increased, more voltage dropped across the resistor and less current flowed, making the LED visibly dimmer. Changing R1 is an effective way to control LED brightness and limit current.

**Images**

<img src="https://github.com/jithk03/Portfolio/blob/dfe74bb40e2cb30c9ab6303fa952cd94a733bff5/Exercise%201%20EC/Task%201.1%20B.jpeg" width="350" height="350">     <img src="https://github.com/jithk03/Portfolio/blob/dfe74bb40e2cb30c9ab6303fa952cd94a733bff5/Exercise%201%20EC/Taske%201.1.jpeg" width="350" height="350">



---

### Task 1.2 – Switchable LED Circuit

We added a 2-position switch (S1) in series with the LED. When the switch was closed, the LED lit up; when open, the circuit broke and the LED turned off. We also tried connecting the switch in the opposite direction — since it's not polarized, it functioned the same either way. The switch controls the full series current, giving simple on/off control over the LED.

| R1 [Ω] | Measured V1 [V] | Measured V_LED [V] |
|--------|-----------------|--------------------|
| 220    |       2.25      |        2.73        |
| 1000   |       2.18      |        2.74        |
| 4700   |       2.73      |        2.28        |

**Images**

<img src="https://github.com/jithk03/Portfolio/blob/dfe74bb40e2cb30c9ab6303fa952cd94a733bff5/Exercise%201%20EC/Task%201.2.jpeg" width="300" height="300"> <img src="https://github.com/jithk03/Portfolio/blob/dfe74bb40e2cb30c9ab6303fa952cd94a733bff5/Exercise%201%20EC/Task%201.2%20Different%20Resistors.jpeg" width="300" height="300"> 


---

### Task 1.3 – Dimmable LED Circuit

We introduced a 1 kΩ potentiometer (R2) and a fixed 100 Ω resistor (R1) to create a voltage divider that controls the voltage reaching the LED.

**This was the most challenging part of Task 1.** Our first two attempts failed — the LED either stayed fully on or fully off with no dimming in between. We suspected the wiper pin was incorrectly identified and the potentiometer was wired wrong both times. With the professor's help, we correctly identified the middle pin as the wiper (variable output) and rewired the circuit properly. After that, the dimming worked as expected.

| Position           | V_LED [V] | V2 [V] |
|--------------------|-----------|--------|
| a) Full brightness |    2.96   |   2.98 |
| b) Dimmed          |    2.89   |   4.54 |
| c) OFF             |    0.28   |   4.55 |

**Images**

<img src="https://github.com/jithk03/Portfolio/blob/dfe74bb40e2cb30c9ab6303fa952cd94a733bff5/Exercise%201%20EC/Task%201.3.jpeg" width="300" height="300">  
https://github.com/jithk03/Portfolio/blob/main/Exercise%201%20EC/Task%201.3%20Video.mp4


**Observations:** Rotating the potentiometer smoothly varied the voltage at the wiper, giving continuous brightness control — much more practical than swapping resistors as in Task 1.1.

---

## Task 2 – Transistor Switch Circuit

**Goal:** Use an NPN MOSFET (IRLZ44N) to switch and dim a 12V LED strip via PWM. The control side ran on 5V and the load side on 12V, sharing a common ground.

**Components:** Resistors (100 Ω, 10 kΩ), PWM Signal Generator, USB power module, IRLZ44N MOSFET, 2-position switch, 12V LED strip, Breadboard, Jumper wires

> ⚠️ **Do not touch the transistor while powered — it can heat up significantly.**

**MOSFET Pinout (IRLZ44N, TO-220):** Pin 1 = Gate, Pin 2 = Drain, Pin 3 = Source

---

### Task 2.1 – Switchable LED Strip

The LED strip was connected between 12V and the Drain. A gate resistor (Rg = 100 Ω) and pull-down resistor (Rpull = 10 kΩ) were used to safely control the Gate with the 5V switch.

- Switch **closed** → V_GS exceeded threshold → MOSFET ON → LED strip lit up
- Switch **open** → pull-down held Gate at 0V → MOSFET OFF → LED strip dark

The switch controls the **Gate-Source voltage (V_GS)** — a low-power 5V signal switching a high-power 12V load. This is the core principle of MOSFET operation: a voltage-controlled switch with negligible gate current draw.

**Images**

<img src="https://github.com/jithk03/Portfolio/blob/dfe74bb40e2cb30c9ab6303fa952cd94a733bff5/Exercise%201%20EC/Task%202.1.jpeg" width="300" height="350"> <img src="https://github.com/jithk03/Portfolio/blob/main/Exercises%20Pictures/Task%202.2%20B.jpeg?raw=true" width="300" height="210">



> This task required the professor's guidance on the dual power supply setup (5V control + 12V load) and shared ground wiring.

---

### Task 2.2 – Dimmable LED Strip (PWM)

We replaced the manual switch with a PWM Signal Generator (powered from the USB board) to rapidly switch the MOSFET gate on and off at a set frequency and duty cycle.

#### Part A – Duty Cycle (f = 90 Hz, fixed)

| Duty Cycle | Observed Behaviour |
|------------|--------------------|
| D = 2%     | Barely visible |
| D = 15%    | Dimly lit |
| D = 40%    | Moderate brightness |
| D = 75%    | Bright |
| D = 100%   | Full brightness |

**Video**

<img src="https://github.com/jithk03/Portfolio/blob/dfe74bb40e2cb30c9ab6303fa952cd94a733bff5/Exercise%201%20EC/Task%202.2%20B.jpeg" width="300" height="300">
<video src="https://github.com/jithk03/Portfolio/blob/a8955b0115042e8b45d1c46a659389bbc8fa61ff/Exercises%20Pictures/Task%202.2.mp4?raw=true" width="300" height="240" controls></video>



Higher duty cycle = more time ON = higher average power = brighter strip. Unlike the potentiometer (which wastes energy as heat), PWM is efficient — the MOSFET is either fully ON or fully OFF.

#### Part B – Switching Frequency (D = 50%, fixed)

| Frequency | Observed Behaviour |
|-----------|--------------------|
| f = 5 Hz  | Clearly visible slow flashing |
| f = 25 Hz | Rapid, uncomfortable flicker |
| f = 45 Hz | Flicker at edge of perception |
| f = 100 Hz| Steady glow — flicker no longer visible |

At low frequencies the eye can detect individual on/off cycles. Above ~50–60 Hz, flicker becomes imperceptible and the strip appears to glow steadily at reduced brightness.

<img src="https://github.com/jithk03/Portfolio/blob/dfe74bb40e2cb30c9ab6303fa952cd94a733bff5/Exercise%201%20EC/Task%202.2%20B.jpeg" width="300" height="300">
---

## Summary

| Task | Key Concept |
|------|-------------|
| 1.1 | Current limiting, Ohm's Law |
| 1.2 | Series switching (on/off) |
| 1.3 | Analogue dimming via potentiometer *(required professor's help after two failed attempts)* |
| 2.1 | MOSFET as a transistor switch |
| 2.2 | PWM dimming — duty cycle and flicker frequency |

---

*Digital Design & Fabrication — Exercise 1 | Carl von Ossietzky Universität Oldenburg*
