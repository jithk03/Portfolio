# Exercise 6 — Laser Cut Business Cards
### Digital Design and Fabrication (inf175) · Carl von Ossietzky Universität Oldenburg

---

## Table of Contents
1. [Overview](#overview)
2. [Design Process](#design-process)
3. [Material & Settings Configuration](#material--settings-configuration)
4. [Measuring Material Thickness](#measuring-material-thickness)
5. [Cutting Process](#cutting-process)
6. [Final Result](#final-result)
7. [Summary](#summary)

---

## Overview

This project is part of the **Digital Design and Fabrication** course (inf175). The goal was to design and fabricate a laser-cut business card using **Inkscape** and a laser cutter in the university lab.

**Requirements:**
- Standard business card dimensions: **89 × 51 mm**
- Use of both **vector** (cut/score lines) and **raster** (engraving) modes
- Cut-out fonts with **bridges** to prevent floating islands
- Design aligned to the **top-left corner** with a **1 mm margin**
- Material: MDF plywood (or cardboard / acrylic)

---

## Design Process

### Concept & Inkscape File

<img src="https://github.com/jithk03/Portfolio/blob/7164a201a02c8aab73255100a461e933cad102e4/Exercise%206/Jithu%20.jpeg" length="350" width="350">
| Figure 1 — Final Inkscape layout (89 × 51 mm, 1 mm margin from top-left)* |

**Design decisions:**
- **Vector layer** (red stroke, 0.001" line width): outer card outline + cut-out letters/shapes
- **Raster layer** (black fill): engraved name, title, contact details, logo/graphic
- Bridges added to enclosed letters (e.g. **A, B, D, O, P, Q, R**) to keep inner parts attached
- Font chosen for legibility at small scale after engraving

---

## Material & Settings Configuration

### Material
| Property | Value |
|---|---|
| Material | MDF Plywood |
| Nominal thickness | 3 mm (measured: see below) |
| Dimensions used | 89 × 51 mm |

### Laser Cutter Settings

> _Fill in the actual values you used in the lab._

| Operation | Speed (%) | Power (%) | Passes | Notes |
|---|---|---|---|---|
| Raster engrave | | | 1 | Engraving text & graphics |
| Vector score | | | 1 | Decorative lines / folds |
| Vector cut (outline) | | | 1–2 | Full cut-through |

<!-- Photos of the software/settings screen on the laser cutter -->
| Settings — Software Configuration |
|:---:|
<img src="https://github.com/jithk03/Portfolio/blob/7164a201a02c8aab73255100a461e933cad102e4/Exercise%206/First.jpeg" length="400" width="400">
| *Figure 2 — Laser cutter job settings in the control software* |

| Settings — Machine Control Panel |
|:---:|
| ![Machine panel](images/settings_panel.jpg) |
| *Figure 3 — Power and speed settings on the machine panel* |

---

## Measuring Material Thickness

Accurate thickness measurement is critical for setting the correct **focus height** on the laser cutter.

| Measurement Tool | Measured Thickness |
|---|---|
| Digital caliper | ___ mm |

<!-- Photos of measuring the MDF sheet with calipers -->
| Measuring with Digital Caliper |
|:---:|
| ![Thickness measurement 1](images/measure_caliper_1.jpg) |
| *Figure 4 — Measuring the MDF plywood at point 1* |

| | |
|:---:|:---:|
| ![Thickness measurement 2](images/measure_caliper_2.jpg) | ![Thickness measurement 3](images/measure_caliper_3.jpg) |
| *Figure 5 — Measurement at point 2* | *Figure 6 — Measurement at point 3 (edge)* |

> **Note:** MDF thickness can vary slightly across the sheet. Take at least 3 measurements and use the average for focus calibration.

---

## Cutting Process

### Step-by-step

1. Exported Inkscape file as `.svg` / `.pdf` and imported into the laser cutter software
2. Set origin at top-left corner of the material
3. Ran a **test engrave** on a scrap piece to verify settings
4. Placed the MDF sheet and ran the **raster job** first, then the **vector cut**

<!-- Photos and videos of the cutting process -->

| Bed Setup — Material Positioned |
|:---:|
| ![Bed setup](images/cutting_bed_setup.jpg) |
| *Figure 7 — MDF sheet positioned on the laser cutter bed* |

| Engraving in Progress |
|:---:|
| ![Engraving process](images/cutting_engraving.jpg) |
| *Figure 8 — Raster engraving pass running* |

| Vector Cutting in Progress |
|:---:|
| ![Vector cutting](images/cutting_vector.jpg) |
| *Figure 9 — Vector cut (outline) running* |

### Process Video

> _Embed or link a video of the cutting process below._

<!-- Option A: GitHub hosted video (MP4 < 10 MB) -->
https://github.com/YOUR_USERNAME/YOUR_REPO/raw/main/videos/cutting_process.mp4

<!-- Option B: YouTube / unlisted link -->
[![Cutting process video](images/cutting_video_thumbnail.jpg)](https://youtu.be/YOUR_VIDEO_ID)
*Video 1 — Laser cutting the business card*

---

## Final Result

| Front of Card |
|:---:|
| ![Final card front](images/final_front.jpg) |
| *Figure 10 — Final laser-cut business card (front)* |

| Back of Card | Card in Hand |
|:---:|:---:|
| ![Final card back](images/final_back.jpg) | ![Card in hand](images/final_in_hand.jpg) |
| *Figure 11 — Back side* | *Figure 12 — Scale reference* |

**Observations:**
- Engraving quality: _e.g. crisp / slightly burned edges_
- Cut quality: _e.g. clean edges, slight charring removed by wiping_
- Bridges: _held up well / required light sanding_

---

## Failed Attempts & Reflections

### Attempt 1

| Failed Attempt 1 |
|:---:|
| ![Failed attempt 1](images/failed_attempt_1.jpg) |
| *Figure 13 — First failed attempt* |

**What went wrong:**
> _e.g. Power too high — burned through fine details. The engraving pass scorched the surface around letters._

**What I changed:**
> _e.g. Reduced power from 80% → 60% and increased speed from 40% → 55%._

---

### Attempt 2 *(if applicable)*

| Failed Attempt 2 |
|:---:|
| ![Failed attempt 2](images/failed_attempt_2.jpg) |
| *Figure 14 — Second failed attempt* |

**What went wrong:**
> _e.g. Focus height was off — cut did not go all the way through in one pass._

**What I changed:**
> _e.g. Re-measured material thickness (was 3.2 mm, not 3.0 mm) and recalibrated focus._

---

## Summary

| | |
|---|---|
| **Course** | Digital Design and Fabrication (inf175) |
| **Exercise** | 6 — Laser Cut Business Cards |
| **Tool** | Inkscape + Laser cutter (lab) |
| **Material** | MDF Plywood, ~3 mm |
| **Techniques** | Vector cut, raster engrave, bridges for cut-out type |
| **Date** | June 2026 |

> **Inspiration:** [MIT HCIE — Laser Cut Business Card examples](https://hcie.csail.mit.edu/classes/2021-fall6810/laser-cut-business-card.html)

---

*Report by [Your Name] · inf175 · Universität Oldenburg*
