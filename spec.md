# Project specification

# Beam Designer

## Purpose
Shear, moment, and deflection diagrams for a beam, with a check of
whether the beam is strong and stiff enough.

## Inputs
- Simply supported or cantilever, and the span (ft)
- A steel W-shape or dimensional lumber, using built-in property defaults or custom-entered beam properties
- Point loads and uniform loads over the full span
- An option to include or exclude beam self-weight
- A user-selected design method: ASD or LRFD

## Calculations
- Reactions, shear, and moment from statics
- Deflection
- Code-based bending capacity using AISC 360 for steel or NDS for lumber
- Use the code edition specified by the course or project
- Assume steel beams are continuously braced
- Compare deflection to a fixed L/360 limit

## Outputs
- The beam with its loads, and the three diagrams
- Pass or fail for bending and deflection

## Look and feel
Clean and professional, with an example beam loaded when it opens.

## Validation
20 ft simply supported W12x26 with 1 kip/ft: M = 50.0 kip-ft,
deflection 0.609 in.

## Out of scope
Continuous beams and buckling checks; steel beams are assumed continuously braced.