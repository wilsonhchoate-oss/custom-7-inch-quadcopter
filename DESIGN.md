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

## CAD Documentation

The following Fusion 360 CAD renders and engineering drawings document the frame design:

- **Assembly Top View** (`cad/Assembly/Assembly_Top_View.png`): Overview of the complete quadcopter assembly with motor arms, center plates, and electronics stack positioned for reference.
- - **Exploded View** (`cad/Assembly/Exploded_View_png.png`): Detailed breakdown showing how the motor arms, center plates, electronics, and fasteners integrate together.
  - - **Engineering Drawing** (`cad/Drawings/Frame_assembly.png`): Professional engineering drawing with dimensions, bill of materials, and assembly notes derived directly from the Fusion 360 model.7. Slicer orientation and print settings.

## Manufacturing

Record the final settings used:

| Parameter | Final Value |
|---|---|
| Printer | Bambu Lab A1 |
| Material | PETG |
| Nozzle diameter | 0.4 mm |
| Layer height | 0.2 mm |
| Wall loops | 4 |
| Top layers | 4 |
| Bottom layers | 3 |
| Infill percentage | 15% |
| Infill pattern | Gyroid |
| Nozzle temperature | 230 °C |
| Bed temperature | 85 °C |
| Total frame print mass | ~385 g (arms + center plates combined) |

## Design Iteration and Refinement

The final design represents a convergence of mechanical requirements, manufacturability, and assembly accessibility. Key design decisions were driven by:

- **Modularity**: Removable arms allow rapid replacement after impacts without reprinting the entire frame.
- - **Symmetry**: The X-configuration requires matched arm geometry; symmetric plate design simplifies fastening and balance.
  - - **Electronics Integration**: The center-plate assembly was sized around the flight-controller, ESC, and battery stack dimensions to minimize unused internal volume.
    - - **Manufacturing Constraints**: Four wall loops and 15% infill were selected to balance stiffness and print time on the Bambu Lab A1.
     
      - Detailed design iterations and CAD evolution are documented in the Fusion 360 project file; the final configuration reflected in this repository proved structurally sound and flight-capable after testing.
