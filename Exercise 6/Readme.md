# Exercise 6 — Laser Cut Business Cards
### Digital Design and Fabrication (inf175) · Carl von Ossietzky Universität Oldenburg


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
 Figure 1 — Final Inkscape layout (89 × 51 mm, 1 mm margin from top-left)

---

## Material & Settings Configuration

### Material
| Property | Value |
|---|---|
| Material | MDF Plywood |
| Nominal thickness | 3 mm (measured: see below) |
| Dimensions used | 89 × 51 mm |

### Laser Cutter Settings

| Operation | Speed (%) | Power (%) | Passes | Notes |
|---|---|---|---|---|
| Raster engrave | 60 | 100 | 1 | Engraving text & graphics |
| Vector score | 07| 100 | 1 | Decorative lines / folds |
| Vector cut (outline) | | | 1–2 | Full cut-through |

<!-- Photos of the software/settings screen on the laser cutter -->
| Settings — Software Configuration |
|:---:|
| <img src="https://github.com/jithk03/Portfolio/blob/7164a201a02c8aab73255100a461e933cad102e4/Exercise%206/First.jpeg" length="400" width="400"> |
| *Figure 2 — Laser cutter job settings in the control software* |

| Settings — Machine Control Panel |
|:---:|
| <img src="https://github.com/jithk03/Portfolio/blob/cbc67824ef9eeba976d6570d16059278f2499d0d/Exercise%206/manual%20.jpg" length="350" width="350"> |
| *Figure 3 — Power and speed settings on the machine panel* |

---

## Measuring Material Thickness

Accurate thickness measurement is critical for setting the correct **focus height** on the laser cutter.

| Measurement Tool | Measured Thickness |
|---|---|
| Digital caliper | 3.10 mm |

<!-- Photos of measuring the MDF sheet with calipers -->
| Measuring with Digital Caliper |
|:---:|
| <img src="https://github.com/jithk03/Portfolio/blob/0828c450237643b6e3db19b52a81e4f0587ba87c/Exercise%206/Second%20measuring%20thickness.jpeg" height="400" width="400"> |
| *Figure 4 — Measuring the MDF plywood* |


> **Note:** MDF thickness can vary slightly across the sheet. Take at least 3 measurements and use the average for focus calibration.

---

## Cutting Process

### Step-by-step

1. Exported Inkscape file as `.svg` / `.pdf` and imported into the laser cutter software
2. Set origin at top-left corner of the material
3. Ran a **test engrave** on a scrap piece to verify settings
4. Placed the MDF sheet and ran the **raster job** first, then the **vector cut**

<!-- videos of the cutting process -->



### Process Video

<!-- Option B: YouTube / unlisted link -->


https://github.com/jithk03/Portfolio/blob/main/Exercise%206/fourth%20video.mp4

https://github.com/jithk03/Portfolio/blob/main/Exercise%206/Fifth.mp4

*Video 1 — Laser cutting the business card*

---

## Final Result

| Front of Card |
|:---:|
| <img src="https://github.com/jithk03/Portfolio/blob/0828c450237643b6e3db19b52a81e4f0587ba87c/Exercise%206/Final%20output.jpeg" length="400" width="400"> |
| *Figure 10 — Final laser-cut business card (front)* |



**Observations:**
- Engraving quality: _e.g. crisp / slightly burned edges_
- Cut quality: _e.g. clean edges, slight charring removed by wiping_
- Bridges: _held up well / required light sanding_

---


> **Inspiration:** [MIT HCIE — Laser Cut Business Card examples](https://hcie.csail.mit.edu/classes/2021-fall6810/laser-cut-business-card.html)

---

*Report by [Jithu Kennedy] · inf175 · Universität Oldenburg*
