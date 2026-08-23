# Electronics Integration

## System Architecture

```text
3S LiPo
   |
   v
4-in-1 ESC ------> Four brushless motors
   |
   v
Flight Controller
   |
   +------> FlySky receiver via iBUS
   |
   +------> USB connection for Betaflight
```

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
| Firmware | Betaflight 4.5.3 |
| Receiver protocol | iBUS |
| Arm control | AUX switch |
| Motor protocol | Not yet recorded |
| Board alignment | Not yet recorded |
| Channel map | Not yet recorded |
| Failsafe behavior | Not yet recorded |

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
