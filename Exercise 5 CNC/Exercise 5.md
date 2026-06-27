# Exercise 5 | CNC Milling — Tea Light Candle Holder

**Digital Design and Fabrication (inf175)**
Media Informatics and Multimedia Systems

---

## Overview

In this exercise, the goal was to design a wooden tea light candle holder in Inkscape and prepare it for milling on a CNC machine. The task involved creating a vector outline for the candle holder body and placing a precisely-sized circular pocket at its center to hold the tea light candle. The finished sketch was then imported into CAM software, where toolpaths were generated to cut the outline from a block of hardwood and mill out the candle pocket.

A Christmas tree-shaped candle holder was used as the example design for this exercise.

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

## Key Skills Practiced

- Inkscape document setup and unit/page configuration
- Freehand and node-based Bézier path drawing
- Path editing and node type manipulation
- Image tracing and layer management
- Fill/stroke configuration for CAM-ready vector paths
- Precise object sizing and alignment tools
- Translating 2D vector designs into CNC toolpaths

## Reflection

*(Add your personal notes here: what design you chose, any challenges encountered while drawing the outline or aligning the pocket, how the milling turned out, and what you would do differently next time.)*

## Pictures

### Vector Design (Inkscape)

*(Insert a screenshot of your finished outline + candle pocket in Inkscape here.)*

```markdown
![Inkscape design](./images/inkscape-design.png)
```

### CAM Toolpaths

*(Insert a screenshot of the generated toolpaths from the CAM software here.)*

```markdown
![CAM toolpaths](./images/cam-toolpaths.png)
```

### Milling Process

*(Insert photos of the CNC machine milling the design here.)*

```markdown
![Milling in progress](./images/milling-process.png)
```

### Final Result

*(Insert photos of the finished wooden tea light candle holder here — multiple angles recommended.)*

```markdown
![Final candle holder](./images/final-result.png)
```

### Failed Attempts / Issues *(optional)*

*(If applicable, insert photos of any failed attempts along with a short note on what went wrong and how it was fixed.)*

```markdown
![Failed attempt](./images/failed-attempt.png)
```
