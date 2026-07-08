# 3D Printing Exercise – Batman Logo Keychain

## What I modeled and why

For this exercise I ended up making two things. My first attempt was a mobile stand, but it got rejected because it didn't fit the printer's build constraints properly and the filament usage went above the 120 g limit once supports were factored in, so I had to scrap that idea and start over.

My second (and final) design was a Batman logo keychain with the word "vengeance" cut into the sketch. I wanted something small, practical, and a bit fun to carry around — a keychain felt like a good fit for the size and weight limits, and it gave me a chance to practice sketching more complex, non-geometric shapes instead of just boxes and cylinders.


## Intial Design

<img src="https://github.com/jithk03/Portfolio/blob/b5a1c6cbb5799c1c8cf98a2de18fa7b26f3ed290/Exercise%208/Intial%20Design.png">
This was my intial Design

## Modeling process

To get the Batman logo shape right, I imported a JPEG reference image into the sketch and used it as a guide to trace the outline. I used a mix of the line tool and the spline tool to build the outline — the spline tool especially for the curved parts of the logo, since straight lines obviously wouldn't cut it for something like that.

This part was genuinely difficult. Getting the curves to actually look like the Batman logo (and not some rough approximation of it) took several attempts — a lot of redoing sections of the spline until the proportions looked right. Once the outline was done, I extruded the sketch downward with a depth of 6 mm, and used the text tool to add the word "vengeance" into the sketch as well.

Overall, turning the idea into an actual model was harder than I expected, mostly because of the curve-matching work. The extrude and text steps themselves were straightforward once the sketch was solid.

## Slicing (QIDI Studio)

For slicing, I kept things fairly simple:

- **Orientation:** default, top-down view of the logo (flat on the bed)
- **Supports:** enabled a small support tree at a 40° threshold angle
- **Other settings:** left at the lab manual defaults (filament: PLA Rapido, printer: QIDI Q2)

Slicing completed without errors. Final estimated stats:

- **Filament used:** 19 g
- **Print time:** ~19–20 minutes

Both comfortably within the 120 g / build volume limits.

## Final result

<img src="https://github.com/jithk03/Portfolio/blob/64d9735a4d3a087a531e475871d924b70f479047/Exercise%208/IMG_1500.jpg" height="450" width="400">
<img src="https://github.com/jithk03/Portfolio/blob/64d9735a4d3a087a531e475871d924b70f479047/Exercise%208/IMG_1501.jpg" height="450" width="400">

The final printed result came out clean and accurate, with smooth surface quality and well-defined edges. The dimensions were consistent with the design intent and no major printing artefacts were visible. The extruded portion in particular came out remarkably well, capturing the depth and form exactly as modelled. The finished piece is compact and lightweight, making it perfectly suited for use as a keychain, a practical and functional outcome from the exercise.
