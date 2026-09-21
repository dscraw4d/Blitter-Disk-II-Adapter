# RP2350 Firmware

**Status: planned - not implemented in Revision B.**

The intended firmware will run on a Raspberry Pi Pico 2 / RP2350 and provide deterministic Disk II control independent of USB host latency.

Planned responsibilities:

- safe startup with drive disabled and writing blocked
- PH0-PH3 stepper control
- motor/drive enable control
- read-data timing capture with PIO
- write-data pulse generation with PIO
- write-protect reporting
- seek/home logic
- USB command protocol
- read/write timeouts and fail-safe reset behavior

Firmware contributions should preserve the hardware rule that write capability remains disabled unless both software and the physical SAFE/WRITE path allow it.
