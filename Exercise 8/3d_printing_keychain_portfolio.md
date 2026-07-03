# 3D Printing Exercise – Batman Logo Keychain

## What I modeled and why

For this exercise I ended up making two things. My first attempt was a mobile stand, but it got rejected because it didn't fit the printer's build constraints properly and the filament usage went above the 120 g limit once supports were factored in, so I had to scrap that idea and start over.

My second (and final) design was a Batman logo keychain with the word "vengeance" cut into the sketch. I wanted something small, practical, and a bit fun to carry around — a keychain felt like a good fit for the size and weight limits, and it gave me a chance to practice sketching more complex, non-geometric shapes instead of just boxes and cylinders.

## First time with parametric CAD

This was my first time using a parametric CAD tool like Onshape. Going in, I didn't have much of an intuition for how sketches, constraints, and extrudes all connect to build up a part, so a lot of the early process was just getting used to how the tool thinks.

## Modeling process

To get the Batman logo shape right, I imported a JPEG reference image into the sketch and used it as a guide to trace the outline. I used a mix of the line tool and the spline tool to build the outline — the spline tool especially for the curved parts of the logo, since straight lines obviously wouldn't cut it for something like that.

This part was genuinely difficult. Getting the curves to actually look like the Batman logo (and not some rough approximation of it) took several attempts — a lot of redoing sections of the spline until the proportions looked right. Once the outline was done, I extruded the sketch downward with a depth of 6 cm, and used the text tool to add the word "vengeance" into the sketch as well.

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

*[Photos of the printed keychain to be added here]*

