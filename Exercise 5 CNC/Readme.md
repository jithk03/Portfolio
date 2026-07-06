# Exercise 5 | CNC Milling — Tea Light Candle Holder

**Digital Design and Fabrication (inf175)**
Media Informatics and Multimedia Systems

---

## Overview

In this exercise, the goal was to design a wooden tea light candle holder in Inkscape and prepare it for milling on a CNC machine. The task involved creating a vector outline for the candle holder body and placing a precisely-sized circular pocket at its center to hold the tea light candle. The finished sketch was then imported into CAM software, where toolpaths were generated to cut the outline from a block of hardwood and mill out the candle pocket.


## Design Process

### 1. Document Setup

- Created a new Inkscape document with display units set to millimetres.
- Set the page size to **100 × 150 mm**, adjusting orientation (portrait/landscape) to suit the design.
- Set the bounding box mode to **Geometric bounding box** under `Edit → Preferences → Tools`, ensuring object dimensions reflect the actual path geometry rather than including stroke width.

### 2. Sketching the Outline

- Used the **Pencil tool** (`P`) to draw the candle holder outline as a Bézier path.
  - Smoothing was set to 45 initially to balance noise reduction with shape accuracy, then fine-tuned.
  - Straight segments were created with single clicks; freehand curves were drawn by holding the left mouse button while dragging.
- Used the **Node tool** (`N`) to refine the path after the initial sketch — adjusting node positions, editing Bézier handles, and converting between smooth, symmetrical, and corner node types to get clean curves and sharp corners where needed.
- For more controlled designs, a reference image (sketch or internet image) was imported via `File → Import`, scaled proportionally using the Selector tool (padlock icon locked to preserve aspect ratio), and moved to the bottom of the layer stack via the **Layers and Objects** panel so the outline could be traced on top of it.
- Path styling was adjusted in `Object → Fill and Stroke`: fill set to **No Paint** and stroke set to a flat colour, with line width adjusted for visibility — important for keeping the design as a clean, single-line vector path suitable for CAM import.

### 3. Candle Pocket and Alignment

- Drew a circle using the **Ellipse/Arc tool**, holding `Ctrl` while dragging to constrain it to a perfect circle.
- Set the circle's width and height to **39.5 mm** using the Selector tool — matching the diameter of a standard tea light candle.
- Positioned the circle at the center of the design using the **Align and Distribute** tool (`Object → Align and Distribute`), aligning it relative to the outline/page rather than placing it by eye.

### 4. From Vector to Toolpath

- The finished SVG was imported into CAM software, where toolpaths were generated for:
  - Cutting the outer profile of the candle holder out of the wood block.
  - Milling the circular pocket to the correct depth for the candle.

## What i Learned...!

- Inkscape document setup and unit/page configuration
- Freehand and node-based Bézier path drawing
- Path editing and node type manipulation
- Image tracing and layer management
- Fill/stroke configuration for CAM-ready vector paths
- Precise object sizing and alignment tools
- Translating 2D vector designs into CNC toolpaths

## Reflection

For this exercise, I designed my own custom shape rather than using the Christmas tree example. Drawing the outline with the Pencil tool turned out to be trickier than expected — my freehand curves came out jagged and uneven rather than smooth, which meant I had to go back in with the Node tool afterward to clean things up by adjusting Bézier handles and merging/removing nodes. In hindsight, relying more on the smoothing setting from the start, or building the curve from fewer, more deliberate node placements instead of a long freehand drag, would likely have given a cleaner result with less rework.

The other main challenge was centering the candle pocket. Even after using the Align and Distribute tool, the circle ended up slightly off-center relative to my outline. This was likely due to aligning the circle relative to the page rather than to the outline itself (or vice versa), since the two reference points can give different results if the design isn't perfectly centered on the page itself. Next time, I'd double-check which alignment reference is selected before relying on the tool, and possibly verify the result numerically (checking X/Y coordinates) rather than just visually.

The final milled piece worked, but came out with a small dimension mismatch versus my original design. This was a minor issue rather than a major failure, but it suggests that something shifted slightly between the Inkscape vector file and the CAM toolpath — possibly during export/import or in how the toolpath software interpreted the path geometry. For future iterations, I'd add a verification step where I measure the design dimensions directly in the CAM software before milling, to catch any discrepancies earlier.

Overall, the piece was usable despite these issues, and the exercise was a good introduction to the gap between a clean-looking digital vector design and the practical precision needed for physical fabrication.

## Pictures

### Vector Design (Inkscape)

<img src="https://github.com/jithk03/Portfolio/blob/b8b28bc26f73a3a91af3beab48b806a28d824a0d/Exercise%205%20CNC/Logo.jpg" length="400" breadth="400">


### Milling Process

https://github.com/jithk03/Portfolio/blob/main/Exercise%205%20CNC/First%20Video.mp4

### Final Result

<img src="https://github.com/jithk03/Portfolio/blob/b8b28bc26f73a3a91af3beab48b806a28d824a0d/Exercise%205%20CNC/Final%201.jpeg" length="350" width="350">

<img src="https://github.com/jithk03/Portfolio/blob/b8b28bc26f73a3a91af3beab48b806a28d824a0d/Exercise%205%20CNC/Final%202.jpeg" length="350" width="350">

