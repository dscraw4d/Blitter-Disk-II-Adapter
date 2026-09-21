# Building the Rev B Prototype

This repository intentionally keeps the complete beginner procedure in one document:

**`docs/Blitter_Disk_II_Adapter_RevB_Beginner_Build_Manual.pdf`**

Use that manual as the authoritative Rev B assembly guide.

## Quick path

1. Read `SAFETY.md`.
2. Review `hardware/diagrams/10_complete_map.png`.
3. Order the parts in `hardware/Blitter_Disk_II_Adapter_RevB_BOM.csv`.
4. Follow `hardware/Blitter_Disk_II_Adapter_RevB_Point_to_Point_Wiring.csv` wire by wire.
5. Build the power section first.
6. Test +12 V, +5 V and -12 V with **no Disk II connected**.
7. Build the RP2350 and logic sections.
8. Verify /ENABLE and /WRREQ default inactive.
9. Verify PH0-PH3 switching using test firmware.
10. Only then power down and connect a real Disk II.

## Current limitation

The Rev B package contains the hardware design and assembly documentation. Production firmware and the Windows/Linux host software are separate future milestones and are not represented as complete in this repository.
