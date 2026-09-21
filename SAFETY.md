# Safety and Vintage-Hardware Protection

The Blitter Disk II Adapter is currently a **prototype**. The purpose of these rules is to reduce the chance of damaging an original Disk II drive or the modern controller.

## The most important rules

1. **Never hot-plug the Disk II 20-pin cable.** Power off the adapter and drive supply before connecting or disconnecting it.
2. **Verify pin 1 twice.** Use a keyed/shrouded 2x10 connector and mark the red-stripe side of the ribbon cable.
3. **Test with the Disk II disconnected first.** Measure every power rail and idle control signal at J2.
4. **Do not power the Disk II from USB.** The vintage drive uses separate +12 V, +5 V and -12 V rails.
5. **Keep writing disabled during initial testing.** The hardware SAFE/WRITE switch should remain SAFE until read-only operation is proven.
6. **Use expendable media for first write tests.** Do not use irreplaceable original disks.
7. **Do not use a solderless breadboard for the drive power rails.** Build the power path on PCB/perfboard with secure connections.

## Before connecting a drive

With J2 empty, confirm relative to ground:

- pins 13, 15, 17, 19: approximately +12 V
- pins 11, 12: +5.0 V
- pin 9: approximately -12 V
- pins 1, 3, 5, 7: ground
- /ENABLE: HIGH / inactive
- /WRREQ: HIGH / read mode
- WRDATA: inactive

Then exercise PH0-PH3 from test firmware and verify clean valid logic levels before the real drive is attached.

## Project status warning

Rev B has not yet been bench-qualified on vintage hardware. Community review is welcome, but builders assume responsibility for independently checking their own implementation.
