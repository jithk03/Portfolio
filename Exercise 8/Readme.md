# 3D Printing Exercise – Batman Logo Keychain

## What I modeled and why

My design was a Batman logo keychain with the word "vengeance" cut into the sketch. I wanted something small, practical, and a bit fun to carry around — a keychain felt like a good fit for the size and weight limits, and it gave me a chance to practice sketching more complex, non-geometric shapes instead of just boxes and cylinders.
I was not aware that some dimensions had been left unconstrained. I had applied constraints to the main dimensions of the sketch but did not verify that every element was fully defined before proceeding to the extrude. I now understand that a fully constrained sketch — where no geometry is free to move — is essential to producing a reliable and repeatable part, and I will ensure this is checked before leaving the sketch in future work.


## Modeling process

To get the Batman logo shape right, I imported a JPEG reference image into the sketch and used it as a guide to trace the outline. I used a mix of the line tool and the spline tool to build the outline — the spline tool especially for the curved parts of the logo, since straight lines obviously wouldn't cut it for something like that.

Once the outline was done, I extruded the sketch downward with a depth of 6 mm, and used the text tool to add the word "vengeance" into the sketch as well.

Overall, turning the idea into an actual model was harder than I expected. The extrude and text steps themselves were straightforward once the sketch was solid.

## Slicing (QIDI Studio)

For slicing, I kept things fairly simple:

- **Orientation:** default, top-down view of the logo (flat on the bed)
- **Other settings:** left at the lab manual defaults (filament: PLA Rapido, printer: QIDI Q2)

Slicing completed without errors. Final estimated stats:

- **Filament used:** 19 g
- **Print time:** ~19–20 minutes

Both comfortably within the 120 g / build volume limits.

## Final result

<img src="https://github.com/jithk03/Portfolio/blob/64d9735a4d3a087a531e475871d924b70f479047/Exercise%208/IMG_1500.jpg" height="450" width="400">
<img src="https://github.com/jithk03/Portfolio/blob/64d9735a4d3a087a531e475871d924b70f479047/Exercise%208/IMG_1501.jpg" height="450" width="400">

The final printed result came out clean and accurate, with smooth surface quality and well-defined edges.The finished piece is compact and lightweight, making it perfectly suited for use as a keychain, a practical and functional outcome from the exercise.
