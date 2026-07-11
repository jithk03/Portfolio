# Exercise 6 — Laser Cut Business Cards
### Digital Design and Fabrication (inf175) · Carl von Ossietzky Universität Oldenburg


## Overview

This project is part of the **Digital Design and Fabrication** course (inf175). The goal was to design and fabricate a laser-cut business card using **Inkscape** and a laser cutter in the lab.

**Requirements:**
- Standard business card dimensions: **89 × 51 mm**
- Use of both **vector** (cut/score lines) and **raster** (engraving) modes
- Design aligned to the **top-left corner** with a **1 mm margin**
- Material: MDF plywood (or cardboard / acrylic)

---

## Design Process

### Inkscape File

 <img src="https://github.com/jithk03/Portfolio/blob/7164a201a02c8aab73255100a461e933cad102e4/Exercise%206/Jithu%20.jpeg" length="350" width="350"> 
 Final Inkscape layout (89 × 51 mm, 1 mm margin from top-left)

---

## Settings Configuration




<!-- Photos of the software/settings screen on the laser cutter -->
| Settings — Software Configuration |
|:---:|
| <img src="https://github.com/jithk03/Portfolio/blob/7164a201a02c8aab73255100a461e933cad102e4/Exercise%206/First.jpeg" length="400" width="400"> |
| *Laser cutter job settings in the control software* |

| Settings — Machine Control Panel |
|:---:|
| <img src="https://github.com/jithk03/Portfolio/blob/cbc67824ef9eeba976d6570d16059278f2499d0d/Exercise%206/manual%20.jpg" length="350" width="350"> |
| *Power and speed settings on the machine panel* |

---

## Measuring Material Thickness

| Measurement Tool | Measured Thickness |
|---|---|
| Digital caliper | 3.10 mm |

| Measuring with Digital Caliper |
|:---:|
| <img src="https://github.com/jithk03/Portfolio/blob/0828c450237643b6e3db19b52a81e4f0587ba87c/Exercise%206/Second%20measuring%20thickness.jpeg" height="400" width="400"> |
| *Figure  — Measuring the MDF plywood* |

---

### Process Video

<!-- Option B: YouTube / unlisted link -->


https://github.com/jithk03/Portfolio/blob/main/Exercise%206/fourth%20video.mp4



*Video  — Laser cutting the business card*

---

## Final Result

| Front of Card |
|:---:|
| <img src="https://github.com/jithk03/Portfolio/blob/0828c450237643b6e3db19b52a81e4f0587ba87c/Exercise%206/Final%20output.jpeg" length="400" width="400"> |
|  Final laser-cut business card |
The final result of the laser cutting was a perfect business card that was cleanly cut and engraved. It was rewarding to feel the end result after fixing many problems throughout the process, as well as seeing the virtual object turned into a tangible one.


## Reflection

Overall, the exercise produced an acceptable result, though it was not without its challenges along the way.

One of the problems I have had with the card is its borders. Though the border was initially drawn properly and the rest of the card printed successfully, there was some difficulty with the borders. After some investigation, I realized that the issue with the borders was caused by the incorrect settings for the stroke and fill in Inkscape. To make sure that the laser cutter would read the border as a vector cut line, it was necessary to set the width of the stroke to 0.001 mm and fill in the stroke and fill panel to 100%.

The most valuable takeaway from this exercise was learning how to correctly prepare design files for laser cutting, specifically understanding the difference between how vector and raster elements must be set up in the SVG/PDF, and how small configuration details in Inkscape — such as stroke width and fill settings can have a direct and significant impact on the physical fabrication outcome.


