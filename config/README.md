# Configuration Files

## Betaflight Configuration

The final flight-controller configuration is stored as:

- **`betaflight-diff-all.txt`**: Complete Betaflight 4.5.3 configuration dump exported via the CLI `diff all` command. This file captures motor reordering, board alignment (CW0FLIP), pitch offset (180°), accelerometer calibration, receiver protocol (iBUS), and all other settings required to reproduce the exact flight-control behavior.

## Future Documentation

Screenshots of key Betaflight Configurator pages (board alignment visualization, receiver channel mapping, motor test, and OSD settings) would further clarify configuration and serve as reference for future builds or troubleshooting.
