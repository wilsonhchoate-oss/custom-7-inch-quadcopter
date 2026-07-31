# Mechanical Design

## Requirements

The frame needed to:

- Support four A2212 motors and 7-inch propellers.
- Package the flight controller, 4-in-1 ESC, receiver, and battery.
- Be printable on a consumer FDM printer.
- Survive minor low-altitude impacts.
- Allow damaged arms to be replaced.
- Provide access for wiring, fasteners, and the flight-controller USB port.
- Keep total vehicle mass low enough for stable flight.

## Architecture

The selected architecture uses four removable arms captured between top and bottom center plates. This modular approach reduces repair cost and print time after an impact.

## Material Selection

PETG was selected because it provides greater toughness and heat resistance than standard PLA while remaining easy to print on a consumer machine.

## Design Decisions to Document With Images

Add annotated screenshots for:

1. Overall frame dimensions.
2. Arm cross-section and motor mount.
3. Center plate and electronics-stack mounting.
4. Fastener and nut-trap geometry.
5. Arm-to-center-plate interface.
6. Final Fusion 360 assembly.
7. Slicer orientation and print settings.

## Manufacturing

Record the final settings used:

| Parameter | Final Value |
|---|---|
| Printer | Bambu Lab A1 |
| Material | PETG |
| Nozzle diameter | 0.40 mm |
| Layer height | 0.20 mm |
| Wall loops | ADD |
| Top layers | ADD |
| Bottom layers | ADD |
| Infill percentage | 35% |
| Infill pattern | Gyroid |
| Nozzle temperature | ADD |
| Bed temperature | ADD |
| Total frame print mass | ADD |

*(Nozzle diameter, layer height, and infill pulled from the `Overall_frame_dimensions` drawing notes — remaining fields need to be pulled from your slicer profile.)*

## Design Evolution

Include 2–4 images showing how the design changed. For each revision, explain:

- What was wrong with the prior version.
- What changed.
- Why the change improved the design.
- Whether the change affected mass, stiffness, print time, or assembly.
