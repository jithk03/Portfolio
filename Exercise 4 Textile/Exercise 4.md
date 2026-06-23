# Exercise 4: E-Textiles — LED Patch
### Physical Computing (inf175) — Portfolio Entry
> Carl von Ossietzky Universität Oldenburg | Summer Term 2026

---

## Overview

In this exercise, we designed and hand-sewn an e-textile patch that can be attached to clothing. Using conductive thread, sewable LEDs, and a 3V coin battery holder, we built a soft circuit embedded into fabric. The goal was to gain hands-on experience with functional materials, understand soft circuit design, and learn to deal with the unexpected setbacks that come with working in this medium.

---

## Materials Used

| Material | Purpose |
|----------|---------|
| Sewable 3V coin battery holder | Power source for the circuit |
| Sewable LEDs (×5+) | Light elements of the patch |
| Conductive thread | Electrical conductor replacing wires |
| Sewing needle + needle threader | Hand sewing |
| Fabric pen / chalk | Marking circuit paths on fabric |
| Scissors | Cutting fabric and thread |
| Nail polish | Insulating thread crossings to prevent short circuits |
| Masking tape | Temporarily holding components in place |

> ⚠️ Conductive thread (copper-based) is very difficult to recycle — we used it economically and collected all cut-offs for reuse.

---

## Patch Design

We designed a custom patch in an **eye-like organic shape** — not a perfect eye, but a curved, leaf-shaped form with a pointed ends. We first created a paper template to plan the layout before cutting the fabric, which helped us plan the exact positions of the LEDs and battery holder and estimate the thread lengths needed.

The base textile was cut to the shape, and the cover piece was prepared separately. Component positions were marked with fabric pen before any sewing began.

<img src="https://github.com/jithk03/Portfolio/blob/824ef3a0aca806005f2cbd04faa177b90d946a6e/Exercise%204%20Textile/Intial%20design.jpeg" height="400" width= "400">

---

## Circuit Design — Parallel Circuit

We chose a **parallel circuit** to connect all LEDs to the battery holder. This was the correct choice for this type of e-textile circuit for two reasons:

- Conductive thread itself has relatively high resistance, so a series circuit would have added too much total resistance — not all LEDs would have lit up.
- In a parallel circuit, each LED receives the same constant voltage directly from the battery, regardless of how many LEDs are connected. All LEDs light up at full brightness.

Each LED's positive leg (anode) was connected to the positive rail of the battery holder, and each negative leg (cathode) to the negative rail, using separate runs of conductive thread.

---

## Sewing Process

We followed these steps:

1. Created a paper template and marked component positions on fabric.
2. Placed the battery holder at the center and all 5 LEDs around the shape.
3. Temporarily secured components with masking tape.
4. Began hand-sewing the positive rail first, connecting battery (+) to each LED anode using back stitch with conductive thread.
5. Sewed the negative rail separately, connecting battery (−) to each LED cathode.
6. Attached the base textile to the cover piece.
7. Added velcro on the back for attaching to clothing.

**Stitch technique used:** Back stitch for the conductive thread runs — this gives the most reliable electrical contact. Regular (non-conductive) hemming stitch was used to attach the cover piece.

<img src="https://github.com/jithk03/Portfolio/blob/824ef3a0aca806005f2cbd04faa177b90d946a6e/Exercise%204%20Textile/with%203%20leds.jpeg" height="370" width="350">

---

## Challenges — Short Circuits from Crossing Threads

**This was the most difficult part of the exercise.** We had to redo the stitching several times because the conductive thread from the positive and negative rails crossed or touched each other at certain points on the patch, causing short circuits. When this happened, the circuit would either not work at all or the battery would drain immediately.

**How we identified the problem:** When the battery was inserted and no LEDs lit up (or the battery got warm), we knew a short circuit was present. We used the multimeter in continuity mode to trace where the two rails were unintentionally making contact.

**How we fixed it:** We carefully unpicked the stitching at the crossing points and re-routed the thread to avoid overlap. Where crossings were unavoidable, we applied a small drop of **nail polish** over one thread to insulate it at that point, then let it dry before continuing. This is the standard technique for handling thread crossings in e-textile circuits.

After redoing the stitching with proper separation between the positive and negative rails, the short circuits were eliminated.

#### ❌ Failed Attempt — Short Circuit

<img src="https://github.com/jithk03/Portfolio/blob/824ef3a0aca806005f2cbd04faa177b90d946a6e/Exercise%204%20Textile/failed.jpeg" height="350" width="340">

> *Above: The positive and negative conductive thread rails crossing/touching, causing a short circuit. No LEDs lit up at this stage.*

---

## Final Result

After correcting all short circuits and completing the stitching, all 5 LEDs lit up successfully when the coin battery was inserted. The patch holds its shape and can be attached to clothing via the velcro backing.

#### ✅ Final Patch — LEDs Lit

<img src="https://github.com/jithk03/Portfolio/blob/824ef3a0aca806005f2cbd04faa177b90d946a6e/Exercise%204%20Textile/final.jpeg" height="380" width="350">

---

### 🎥 Final Output

https://github.com/jithk03/Portfolio/blob/522494fc9805a360614c209e499b211836d2e6a0/Exercise%204%20Textile/Final%20video.mp4


---

## Reflection

This exercise was a genuinely different experience from the previous ones. Moving from breadboards and jumper wires to needle and thread required a completely different kind of precision — instead of worrying about pin connections, we had to think spatially about routing thread paths across fabric without them ever touching.

**What worked well:**
- Choosing a parallel circuit from the start meant all LEDs received sufficient voltage and lit up at full brightness.
- Creating a paper template first saved a lot of material and made component placement straightforward.
- The nail polish trick for insulating crossing threads was simple and effective once we knew about it.

**What was difficult:**
- Keeping the positive and negative thread rails completely separate while hand-sewing was harder than expected — the thread has a tendency to stray, especially around curves.
- Identifying where exactly a short circuit was occurring required patience and systematic checking with the multimeter.
- Undoing conductive stitches without damaging the fabric or LEDs took care.

**What we would do differently:**
Plan the thread routing more carefully before sewing — draw both rails on the fabric with fabric pen before starting, so crossing points are identified and insulated proactively rather than discovered after the short circuit occurs.

---

## Summary

| Step | Description | Outcome |
|------|-------------|---------|
| Design | Eye-shaped organic patch, paper template first | ✅ Completed |
| Circuit choice | Parallel circuit — all LEDs connected to same voltage | ✅ Correct choice |
| Sewing | Hand-sewn with conductive thread, back stitch | ⚠️ Required multiple redos due to short circuits |
| Short circuit fix | Thread re-routed + nail polish insulation at crossings | ✅ Resolved |
| Final patch | All 5 LEDs lit, velcro backing attached | ✅ Fully working |

---

*Physical Computing (inf175) — Exercise 4 | Carl von Ossietzky Universität Oldenburg*
