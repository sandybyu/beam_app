# Beam Designer

## Purpose
An educational beam screening tool for engineers and students. The user
sets up a beam, applies loads, and selects a steel or lumber section. The
app updates shear, moment, and deflection diagrams and simple pass/fail
checks as inputs change.

## Inputs
- Support: simply supported or cantilever fixed at the left end.
- Span: 4 to 40 ft.
- Section: one of the steel W-shapes or Douglas Fir-Larch No. 2 sizes in
  the professor-provided tables, or custom-entered section properties.
- Point loads: magnitude in kips and position in ft.
- Uniform loads: magnitude in kips/ft and start/end positions in ft;
  loads are clipped to the beam span.
- Loads are downward-positive. Point loads can be dragged along the beam
  and snap to 0.25 ft.
- Deflection limit: L/240 or L/360, default L/360.
- Self-weight is ignored.

## Calculations
- Reactions, shear, and moment from statics
- Deflection by integrating moment over EI with the support boundary
  conditions.
- Bending stress: `fb = |Mmax| * 12 / Sx`, compared with the fixed
  reference `Fb` supplied for the selected table.
- Deflection compared with the selected L/240 or L/360 limit.
- Recommend the lightest passing steel section by weight (ties use larger
  Ix), or the first passing lumber size in the table.
- Use the professor-provided E, I, S, Fb, and steel weight values.

These are simplified educational screening checks. They are not full
AISC 360 or NDS design calculations and do not implement ASD or LRFD.

## Outputs
- The beam with its loads, and the three diagrams
- Pass or fail for bending and deflection
- Support reactions and fixed-end moment where applicable
- Hover readout for shear, moment, and deflection along the span
- Lightest passing section suggestion

## Look and feel
Clean and professional, with an example beam loaded when it opens.
Inputs are on the left and diagrams/checks on the right, with a stacked
layout on narrow screens.

## Validation
20 ft simply supported W12x26 with 1 kip/ft: M = 50.0 kip-ft,
deflection 0.609 in.

## Out of scope
Self-weight, shear stress, lateral-torsional buckling, load combinations,
continuous beams, and saving designs.