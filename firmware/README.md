# Firmware — ESP32

Firmware for the **AutoVolt** automatic battery charger, running on the **ESP32**.

The firmware is responsible for driving the full charge cycle:

1. Detect an empty battery loaded into the charging slot
2. Enable charging via the TP4056 module
3. Monitor battery voltage through the ADC and track charge completion
4. Trigger the MG90S servo to dispense the charged battery
5. Signal readiness for the next empty battery

## Overview

Early-stage project — this firmware is a work in progress.

## Platform

- **MCU:** ESP32
- **Target board:** TBD

## Directory Layout

```
firmware/
├── include/     → Header files
├── src/
│   └── main.c   → Firmware entry point
└── README.md
```

## Build & Flash

Build and flash scripts are prepared at the repository root (`scripts/build.sh`, `scripts/flash.sh`) and will be documented here once the toolchain/build system is finalized.

## Pin Mapping

| Function              | GPIO | Notes                        |
|-----------------------|------|------------------------------|
| Servo PWM (MG90S)     | TBD  | Load/dispense mechanism      |
| TP4056 charge status  | TBD  | Charge-in-progress indicator |
| Slot 1 voltage (ADC)  | TBD  | Battery voltage monitoring   |
| Slot 2 voltage (ADC)  | TBD  | Battery voltage monitoring   |
| Battery present slot 1| TBD  | Empty battery inserted       |
| Battery present slot 2| TBD  | Empty battery inserted       |

_Pin assignments are not finalized._