# Electronics Integration

## Wiring Documentation

Add a clear wiring diagram and close-up photographs. Label:

- Battery positive and ground
- ESC-to-flight-controller connection
- Motor outputs 1–4
- Receiver 5 V, ground, and iBUS signal
- Flight-controller orientation arrow
- USB access direction

## Configuration Summary

| Setting | Value |
|---|---|
| Firmware | Betaflight 4.5.3 (May 26 2025) |
| Receiver protocol | iBUS |
| Arm control | AUX 0 (1800–2100 μs) |
| Motor protocol | DShot600 (from motor reordering: 0,2,1,3) |
| Board alignment | CW0FLIP, Pitch 180° |
| Yaw motors | Reversed |
| Failsafe behavior | Default (land on signal loss) |
| Accelerometer calibration | (6, -72, -50) applied on level surface |

## Quality Checks

- Inspected solder joints.
- Verified polarity before power-up.
- Used a smoke stopper during initial power testing.
- Tested receiver channels in Betaflight.
- Tested each motor individually without propellers.
- Confirmed motor direction and motor numbering.
- Secured and insulated wiring before flight.

## Betaflight Backup

Export the final configuration using the Betaflight CLI:

```text
diff all
```

Save the output as:

```text
config/betaflight-diff-all.txt
```

Do not publish Wi-Fi passwords, personal information, serial numbers you consider private, or unrelated device data.
