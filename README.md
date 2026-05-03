# My Portfolio
Hi Iam Jithu Kennedy
🎓 Master’s Student: Socio-Technical Systems (Sem. 2)
<br>
🛠️ Currently: Exploring Digital Design & Fabrication
<br>
📍 University of Oldenburg

This portfolio is a raw look at my fabrication projects. I share the wins, the losses, and the technical iterations that happen in between. Join me as I build, break, and learn.
<br>
My Immatriculation No:6645377
<br>
University Email id: jithu.kennedy@uni-oldenburg.de

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
![image alt](https://github.com/jithk03/Portfolio/blob/main/Exercises%20Pictures/Taske%201.1.jpeg?raw=true)

---

### Task 1.2 – Switchable LED Circuit

We added a 2-position switch (S1) in series with the LED. When the switch was closed, the LED lit up; when open, the circuit broke and the LED turned off. We also tried connecting the switch in the opposite direction — since it's not polarized, it functioned the same either way. The switch controls the full series current, giving simple on/off control over the LED.

---
