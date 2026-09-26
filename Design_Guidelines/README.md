# Design guidelines

General design criteria, independent of the third-party toolhead list.

## Toolhead integration CAD

[Toolhead integration STEP](CAD/Toolhead_Integration.step): Simplified gantry geometry for checking toolhead clearance.

Includes AWD full Y travel, AWD FT-FT without Y overtravel, and 2WD full Y travel. Show one scenario at a time.

## Belt retention

- Match Monolith's flipped belt orientation, belt spacing, and selected belt width.
- Follow Gates' tooth-engagement and minimum bend-radius guidance.
- Belt retention and the toolhead must support the target belt tension. Otherwise reduce tension to the limit of the weakest motion-system or frame component.
- Retention geometry, worst to best:
    - sharp-edged wrap, few engaged teeth
    - rounded-pin wrap, tight bend and few engaged teeth
    - sufficient engagement, tight loaded-path bend
    - straight clamp, at least six engaged teeth and no loaded-path bend on the toolhead (Monolith target).

## Stiffness and center of mass

- Evaluate the complete printer/toolhead system: total mass, center of mass, carriage stiffness, and the hotend and extruder mounts, including their attachment to the carriage.
- A metal carriage can reduce carriage deflection under belt tension, but it does not remove flexibility in printed hotend and extruder mounts.

## Clearance and endstops

- X travel and AWD front clearance depend on the toolhead.
- Physical X and Y endstop switches and sensorless homing are supported.
- The gantry-side X switch mounts to the Y extrusion because toolheads, carriages, and XY-joints do not share one universal toolhead-mounted switch position. Home Y before X when using it.
