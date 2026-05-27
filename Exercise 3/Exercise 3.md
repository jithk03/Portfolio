# Exercise 3: Sensors & Actuators — Pneumatic System
### Digital Design & Fabrication — Portfolio Entry
> Carl von Ossietzky Universität Oldenburg

---

## Overview

In this exercise, we built a pneumatic system consisting of two air pumps, an air valve, and an inflatable pillow — controlled by an Arduino Uno via MOSFET driver modules. The creative challenge was to design a sensor-driven interaction that triggers inflation and deflation. We used **two ultrasonic distance sensors** as the input interface: covering the left sensor with your hand inflates the pillow, and covering the right sensor deflates it — a direct, intuitive two-handed control.

The exercise was split into two parallel threads — Part A (pneumatic & electrical circuit) and Part B (sensor interaction) — which we then combined into the final working system.

---

## Components Used

| Component | Spec | Role |
|-----------|------|------|
| Air Pump ZR370-02PM (×2) | 4.5V, ~500mA | One inflates, one deflates |
| Air Valve FA0520E (×1) | 6V, ~400mA, 3 ports | Switches air path between pumps |
| MOSFET Driver Module IRF520 (×3) | 3.3–5V control, 0–24V load | One per actuator |
| Arduino Uno | USB powered | Microcontroller |
| Ultrasonic Distance Sensor HC-SR04 (×2) | — | Left = inflate trigger, Right = deflate trigger |
| Lab Power Supply | 5V, current limited | Powers pumps and valve |

---

## Part A — Pneumatic & Electrical Circuit

### How the MOSFET Modules Work

Each IRF520 MOSFET module sits between the Arduino and a high-current actuator (pump or valve). The Arduino sends a digital HIGH or LOW to the module's SIG pin — HIGH turns the load ON, LOW turns it OFF. The load side is powered separately from the lab power supply, with a shared common ground connecting both sides. Each module has a built-in status LED that lights up when the MOSFET is conducting — very useful for debugging.

### Pneumatic Circuit Logic

The valve (FA0520E) has three ports and acts like a pneumatic relay:
- **Unpowered** → common port connected to metal-end port (inflation path open)
- **Powered** → common port switches to plastic-end port (deflation path open)

By combining the valve state with which pump is running, we could switch between inflating and deflating the pillow.

### What Went Wrong — and How We Fixed It

When we first completed the circuit, the **pillow inflated but would not deflate**. We tried fixing it ourselves — checking tubing connections, swapping pump outputs, reviewing the code — but could not isolate the issue.

The root cause was **confusion around the MOSFET module wiring**. We had misconnected the control-side GND and SIG pins on one of the modules, meaning the deflation pump's MOSFET was never actually switching. The valve port assignments also weren't immediately intuitive — even when the valve was powered, the air path wasn't switching correctly because the common port was mapped wrong.

With the professor's help, we corrected the MOSFET wiring and re-mapped the valve ports properly. After that, both inflation and deflation worked correctly.

#### ❌ Failed Experiment



https://github.com/user-attachments/assets/797b57c6-2b9d-4d7d-9e3b-d5865a29d757



> *Above: The circuit in its failed state — pillow would only inflate. The MOSFET module for the deflation pump was misconnected (wrong GND and SIG pins), and the valve's common port was incorrectly mapped, preventing the air path from switching.*

---

## Part B — Sensor Interaction Design

### Sensor Choice: Two Ultrasonic Distance Sensors (HC-SR04 × 2)

We used **two HC-SR04 ultrasonic distance sensors** placed side by side as the interaction interface. Each sensor continuously measures the distance in front of it. When a hand is brought close enough to cover a sensor (distance drops below a set threshold), it triggers its corresponding action:

- **Cover the left sensor** → inflation pump turns ON, valve stays unpowered → pillow **inflates**
- **Cover the right sensor** → valve switches, deflation pump turns ON → pillow **deflates**
- **Remove hand** from either sensor → pumps stop

**Why this interaction?**
Rather than using buttons or a single gesture, having two dedicated sensors made the control feel physical and direct — one hand for inflation, one for deflation. It maps naturally to the idea of two separate controls, like a tap with hot and cold. No button presses needed, and the intent of each hand movement is immediately clear.

### How It Works in Code

Both sensors are polled continuously in the main loop. Each reading is compared against a distance threshold (e.g. < 5 cm = hand detected). Depending on which sensor is triggered, the corresponding MOSFET pins are set HIGH or LOW to activate the right pump and valve state. If neither sensor is covered, all actuators stay off.

### Libraries & Resources Used

- `NewPing.h` — simplified HC-SR04 distance readings for both sensors simultaneously.
- HC-SR04 datasheet for pin wiring (VCC, GND, TRIG, ECHO) — two sets of TRIG/ECHO pins used on the Arduino.
- Arduino community tutorials for dual-sensor setup.

---

## Final Combined System

Once both parts were independently verified, we merged them into a single sketch and circuit. The two ultrasonic sensors drove the pump and valve control logic in a continuous loop.

**Result: Fully working.** Both inflation and deflation responded correctly and immediately to hand coverage. The interaction was intuitive — no explanation needed to understand which sensor does what.

#### ✅ Final System



https://github.com/user-attachments/assets/2e33a22b-8f08-4b2d-bc82-a3577d166d0c


---

### 🎥 Demo Video

<!-- Replace with your actual video path or YouTube link -->
[Watch Demo Video](./videos/demo.mp4)

---

## Reflection

This was the most complex exercise so far — stressful at times, but ultimately the most rewarding. Debugging a system with both a pneumatic side and an electronic side simultaneously was genuinely difficult, especially when the issue turned out to be something as subtle as a misconnected MOSFET pin rather than anything in the code.

The moment everything came together — the pillow responding to hand gestures over two sensors in real time — was very satisfying. It felt like everything from previous exercises (resistors, MOSFETs, Arduino, sensors) clicked into a single coherent system.

**What worked well:**
- The two-sensor interaction was intuitive and immediately understandable.
- The MOSFET modules were reliable once correctly wired.
- Working on Part A and Part B separately before combining kept things manageable.

**What was difficult:**
- MOSFET wiring was not immediately obvious — the control-side vs load-side GND distinction caused our initial inflate-only failure.
- Valve port assignments required careful reading of the datasheet to get right.

**What we would explore further:**
Controlling inflation speed proportionally based on how close the hand is to the sensor (closer = faster pump) rather than a simple on/off threshold. A pressure sensor inside the pillow could also add a safety cutoff to prevent over-inflation.

---

## Summary

| Part | Description | Outcome |
|------|-------------|---------|
| Part A — Electrical | MOSFET modules + pumps + valve | ⚠️ Inflate-only at first — MOSFET wiring error fixed with professor's help |
| Part A — Pneumatic | Tubing + valve port mapping | ✅ Correct after wiring fix |
| Part B — Sensor | Dual HC-SR04, left = inflate / right = deflate | ✅ Worked smoothly |
| Combined System | Full sensor-driven inflate/deflate | ✅ Fully working |

---

*Digital Design & Fabrication — Exercise 3 | Carl von Ossietzky Universität Oldenburg*

https://github.com/user-attachments/assets/98eb52ce-690a-40ae-bc06-048dc9d13b1f

