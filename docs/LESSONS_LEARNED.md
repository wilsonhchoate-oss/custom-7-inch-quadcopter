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

## 7. A bad first attempt is still progress

The [Arduino/MPU-6050 prototype](ARDUINO_PROTOTYPE.md) never hovered, and the frame it used wasn't structurally sound enough to survive a real crash. Scrapping it wasn't wasted effort — it's the reason this build uses a dedicated flight-controller/ESC stack instead of a hand-rolled control loop, and the direct reason crash survivability became a hard requirement for the current frame's fastener and joint design.

## 8. Test-site quality is part of the engineering problem, not separate from it

A cramped test area limits how much you can learn about a real issue like hover drift — you can't safely push the vehicle enough to characterize the problem, let alone fix it. Planning for a properly open flight-test site turned out to matter as much as any single tuning parameter. This held up: moving to a genuinely open field resolved the drift completely and produced a stable flight to ~200 ft.

## 9. A structural design is only as good as the impact it was designed for

The fastener/joint design was built to survive minor low-altitude crashes, and it did — repeatedly, with zero damage. A ~200 ft free-fall after an in-flight propeller detachment broke an arm anyway. That's not evidence the design failed; it's evidence the impact was outside the envelope the design was ever rated for. Knowing the difference between "the design failed" and "the event exceeded the design envelope" matters — it changes what you actually fix.

## 10. The checklist is only as good as what's on it

Every pre-flight check up to this point — motor order, motor direction, board orientation, accelerometer calibration, receiver response — was verified individually before this flight. Propeller retention wasn't on that list, and it's the thing that ended the flight. A checklist doesn't protect against the failure mode you didn't think to add.
