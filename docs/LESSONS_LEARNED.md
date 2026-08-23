# Lessons Learned

## 1. System integration is harder than component selection

Every component can work individually while the aircraft still fails as a system. Motor numbering, rotation, propeller orientation, board alignment, radio setup, wiring, and calibration all must agree.

## 2. A failure is useful only when the test isolates variables

Repeatedly attempting takeoff without changing one controlled variable provides little information. Removing propellers and checking motor order, direction, orientation, and receiver response individually made troubleshooting more effective.

## 3. Flight-controller behavior can look like a hardware problem

The controller changes motor outputs to correct attitude error. During restrained or unstable testing, this can sound like uncontrolled throttle increase even though the controller is responding as programmed.

## 4. Mechanical accessibility matters

USB access, solder-pad access, wire routing, fastener clearance, and replaceable parts should be considered during CAD—not after printing.

## 5. Documentation should happen during the build

Photographs of failed revisions, wiring changes, and test setups are more valuable than only showing the finished aircraft. They demonstrate engineering judgment and iteration.

## 6. Successful flight is not the end of the project

A functional prototype creates opportunities for better testing: vibration logging, PID tuning, static thrust measurement, structural analysis, CFD, mass optimization, and autonomous flight.
