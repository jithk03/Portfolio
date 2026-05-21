# Exercise 2: Introduction to Arduino
### Digital Design & Fabrication 
> Carl von Ossietzky Universität Oldenburg

---

## Overview

In this exercise, we built a functional alarm clock using an Arduino Uno, an LCD screen, a buzzer, a Real Time Clock (RTC) module, and push buttons. The exercise was structured around four sub-circuits, each introducing a new component, before combining everything into the final alarm clock system.

We recorded photos and videos of the circuits throughout the session for this portfolio.



---

## Environment Setup

We used the **Arduino IDE** to write and upload code to the Arduino Uno, connected via USB (which also served as the 5V power supply). Required libraries were downloaded from the course page on Stud.IP and installed via `Sketch → Include Library → Add .ZIP Library`:

- `LiquidCrystal_I2C.h` — for the LCD screen
- `RTClib.h` — for the Real Time Clock module
- `Button.h` — for cleaner push button handling (with built-in debouncing)

---

## Sub-circuit 1 – Buzzer

**Components:** Arduino Uno, Buzzer, 220 Ω resistor, Breadboard, Jumper wires

The buzzer was connected to digital pin 13 on the Arduino through a current-limiting resistor (R1 = 220 Ω) to ground. We uploaded the `buzzer_test.ino` sketch and tested different HIGH/LOW sequences and delay durations.

**Observations:** Changing the delay between HIGH and LOW states directly affected the tone and rhythm of the buzzer. Shorter delays produced higher-frequency beeps; longer delays produced slower, more distinct pulses. This sub-circuit went smoothly and gave us a good first feel for how Arduino controls output pins digitally.

> 📸 *Photos and a short video of the buzzer in operation were taken.*

---
<img src="https://github.com/jithk03/Portfolio/blob/main/Excercise%202/E2T1.jpeg" width="350" height="350">  


https://github.com/user-attachments/assets/33f0aaab-157f-4ffa-a9da-8d23d8edcf03



## Sub-circuit 2 – LCD Screen (I2C)

**Components:** Arduino Uno, 2×16 I2C LCD display, Breadboard, Jumper wires

The LCD communicates over the **I2C protocol** using only 4 wires: VCC (5V), GND, SDA (data), and SCL (clock). SDA was connected to Arduino pin A4 and SCL to pin A5.

**I2C Protocol — Brief Explanation:**
I2C uses two wires — SCL sets the timing like a clock, and SDA carries the actual data. Each device on the bus has a unique address; the Arduino (master) sends the target address first, and only the matching device responds. This lets multiple devices share the same two wires.

**This sub-circuit gave us trouble.** We first had to determine the LCD's I2C address using the `I2C_scanner.ino` sketch. The scanner revealed the address was `0x27` — not immediately obvious, and the wiring had to be corrected before the scanner could even detect the device. Once the address was confirmed and wiring fixed with the professor's help, we loaded `LCD_test.ino` and successfully displayed text on the screen.

> 📸 *Photo of the LCD displaying test text was taken.*

---

## Sub-circuit 3 – Real Time Clock (RTC)

**Components:** Arduino Uno, I2C RTC module (with coin cell battery), LCD (carried over), Breadboard, Jumper wires

The RTC module was connected in parallel with the LCD on the same I2C bus (SDA → A4, SCL → A5, VCC → 5V, GND → GND). The coin cell battery inside the module keeps timekeeping running even when the circuit is powered off.

**This sub-circuit also required help.** We ran `I2C_scanner.ino` again with both devices connected and got two addresses — we already knew the LCD address from Sub-circuit 2, so the new address belonged to the RTC. However, we had initial wiring issues where the RTC was not being detected at all. The professor helped us identify a loose connection on the breadboard. Once corrected, we ran `RTC_LCD_test.ino` and successfully displayed the real time on the LCD screen.

> 📸 *Photo of the RTC + LCD showing live time was taken.*

---

## Sub-circuit 4 – Push Buttons

**Components:** Arduino Uno, Push buttons, Breadboard, Jumper wires

Push buttons have two pairs of legs — each pair is internally connected, and pressing the button bridges the two pairs. We used a multimeter in continuity mode to identify the correct leg pairs before wiring.

We connected the buttons using Arduino's **internal pull-up resistors**, declared in code as:
```cpp
pinMode(2, INPUT_PULLUP);
```
This keeps the pin HIGH by default and reads LOW when the button is pressed — no external pull-down resistor needed. We used the `Button.h` library which handles debouncing automatically, avoiding false readings from contact bounce.

This sub-circuit went without major issues, though understanding the pull-up logic (button reads LOW when pressed, not HIGH) required a moment of adjustment.

> 📸 *Photo of the button wiring on the breadboard was taken.*

---

## Final Task – Alarm Clock

With all four sub-circuits understood, we combined them into a single functional alarm clock circuit on the breadboard.

**Features implemented:**
- Live time displayed on the LCD, sourced from the RTC module
- Alarm time settable via push buttons (without modifying the code)
- Buzzer triggers when the set alarm time is reached
- Alarm dismissal via button press

**Our modifications to the example code:**
We used the provided `DDF_Arduino101_AlarmClock.ino` as our base but modified it to improve the user experience — adjusting the display layout for clearer readability and tweaking the button response logic.

**Result — Partially Working:**
The clock itself functioned correctly — time was displayed accurately on the LCD and updated in real time via the RTC. However, we encountered two issues:

- **The alarm did not trigger reliably** — the time comparison logic in the code had an edge case we could not fully resolve in the session. The buzzer would occasionally fire but not consistently when the alarm time was reached.
- **Button inputs were unreliable** — despite using `Button.h`, one of the buttons behaved erratically, likely due to a loose breadboard connection or a remaining debounce issue in how we integrated it with the alarm-setting logic.

We documented the working state (time display + RTC functioning) and noted the unresolved issues for the portfolio.

> 🎥 *A video of the alarm clock in operation (showing the time display and partial alarm behavior) was recorded.*

---

## Summary

| Sub-circuit | Component | Status |
|-------------|-----------|--------|
| 1 | Buzzer | ✅ Worked smoothly |
| 2 | LCD (I2C) | ⚠️ Address/wiring issues — resolved with professor's help |
| 3 | RTC Module | ⚠️ Connection issue — resolved with professor's help |
| 4 | Push Buttons | ✅ Worked with minor adjustment |
| Final | Alarm Clock | 🔶 Partially working — time display OK, alarm trigger and buttons unreliable |

---

*Digital Design & Fabrication — Exercise 2 | Carl von Ossietzky Universität Oldenburg*
