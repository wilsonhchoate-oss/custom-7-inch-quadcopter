# Testing and Validation

## Test Philosophy

Testing progressed from low-risk subsystem checks to integrated flight tests. Propellers were not installed until receiver input, flight-controller orientation, motor order, and motor direction had been verified.

## Test Matrix

| Test | Configuration | Pass Criteria | Result |
|---|---|---|---|
| Visual inspection | Unpowered | No exposed conductors or loose hardware | PASS |
| Continuity / polarity | Unpowered | No short across battery input | Not recorded |
| Smoke-stopper power-up | Props removed | Normal startup, no overheating | PASS |
| Receiver test | Props removed | Correct channel response and endpoints | PASS |
| Accelerometer test | Props removed | Betaflight model matches physical motion | PASS |
| Individual motor test | Props removed | Correct motor responds | PASS |
| Direction test | Props removed | Each motor matches diagram | PASS |
| One-minute motor run | Props removed | No abnormal heating or vibration | PASS |
| Low-throttle test | Props installed | Symmetric spool-up | PASS |
| Takeoff test | Open area | Clean liftoff without tip-over | PASS AFTER ITERATION |
| Hover test | Low altitude | Sustained controlled hover | PASS |
| Controlled flight | Open area | Pilot can translate and land safely | PASS |

## Failure Analysis

### Takeoff Flip

**Observed behavior:** The aircraft became light on its landing surface and flipped.

**Possible causes evaluated:**

- Incorrect motor order
- Incorrect motor rotation
- Incorrect propeller placement
- Incorrect flight-controller orientation
- Incorrect accelerometer calibration
- Uneven or unstable launch surface
- Wiring or ESC output problem

**Corrective process:**

1. Removed propellers.
2. Verified each motor number in Betaflight.
3. Verified each motor's physical rotation.
4. Matched propellers to the required rotation.
5. Checked the setup model against physical roll, pitch, and yaw movement.
6. Recalibrated the accelerometer on a level surface.
7. Retested on a flat, rigid surface.

**Outcome:** Successful flight was achieved after configuration and assembly checks.

## Flight Evidence to Add

Capture:

- 10–20 second stationary hover from the side.
- Takeoff, short translation, and landing.
- Close-up image of the completed vehicle.
- Top, bottom, and side views.
- One image with the battery installed.
- One image showing the controller and aircraft together.

## Quantitative Data to Add

**Recorded:**
- Takeoff mass: 756 g
- Hover throttle: 40%
- Hover time: 150 s (~2.5 minutes)
- Battery voltage before flight: 12.6 V
- Battery voltage after flight: 12.18 V
- Propeller size: 7-inch, two-blade
- Ambient wind conditions: Calm

**Still needed:**
- Motor temperature after flight (estimated ~55 °C based on ambient and run duration)
- Maximum stable altitude tested (safely tested to ~30 feet; higher altitude capability not yet quantified)

Raw measurements stored in `test-data/flight-test-log.csv`.
