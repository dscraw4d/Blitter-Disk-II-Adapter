# Project Status

## Current revision

**Hardware/documentation revision: B**

**Project state: prototype / pre-bench-validation**

The Rev B documentation is sufficiently detailed for review and prototype construction, but the electrical design has **not yet been declared production-ready or hardware-qualified**.

## Status matrix

| Area | Status | Notes |
|---|---|---|
| System architecture | Documented | Rev B |
| Disk II connector map | Documented | 20-pin mapping included |
| Drive power rails | Documented | +12 V, +5 V, -12 V |
| Output buffering | Documented | 5 V HCT outputs |
| Input buffering | Documented | 3.3 V logic with 5 V-tolerant inputs |
| Write-safety interlock | Documented | hardware SAFE/WRITE concept |
| Point-to-point wiring | Documented | CSV + diagrams |
| Beginner manual | Complete | PDF + DOCX |
| Bench electrical validation | **Pending** | Must be completed before production |
| Real Disk II drive test | **Pending** | No hardware certification yet |
| PCB layout | Planned | KiCad preferred |
| RP2350 firmware | Planned | See `firmware/README.md` |
| USB protocol | Planned | Command + streaming interface |
| DOS 3.3 host filesystem | Planned | Flat directory |
| ProDOS host filesystem | Planned | Directory support |
| Linux live mount | Planned | FUSE |
| Windows live mount | Planned | WinFsp |
| Flux / WOZ support | Future | After stable sector I/O |

## What counts as Rev C

A future Rev C should not be published as hardware-validated until the following are recorded:

1. measured +12 V, +5 V and -12 V rails under load;
2. oscilloscope or logic-analyzer verification of PH0-PH3, /ENABLE, /WRREQ and WRDATA;
3. verified RDDATA and WRPROT input levels;
4. repeated seek/read tests on a sacrificial known-good Disk II;
5. write tests to expendable media with the hardware write interlock verified;
6. thermal and power checks during extended operation.
