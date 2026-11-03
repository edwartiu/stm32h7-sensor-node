# STM32H7 Sensor Node

Attitude and altitude estimation on an STM32H753ZI (Arm Cortex-M7), built from bare metal up: register-level drivers, FreeRTOS, sensor fusion and CAN telemetry.

**Hardware:** NUCLEO-H753ZI, ISM330DHCX 6-DoF IMU, LIS3MDL magnetometer, LPS22HB barometer, 8-channel USB logic analyzer.

## Status
| Phase | Goal | Status |
|---|---|---|
| 1 | Bare-metal bring-up: startup code, linker script, clocks, GPIO, UART, SysTick, GDB over SWD | Not started |
| 2 | Register-level I2C driver; read all 3 sensors; verify with logic analyzer captures | Not started |
| 3 | Sensor drivers with calibration + host unit tests | Not started |
| 4 | FreeRTOS tasks; timing jitter measured | Not started |
| 5 | Attitude (complementary/Madgwick) + barometric altitude, live plot | Not started |
| 6 | FDCAN telemetry + CI | Not started |

## Build
See docs/BUILD.md.
