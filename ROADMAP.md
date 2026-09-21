# Roadmap

The long-term target is a real Apple Disk II drive that behaves like a modern removable filesystem on Windows and Linux.

## Phase 1 - Hardware validation

- build one Rev B prototype
- validate all rails unloaded and loaded
- validate logic directions and idle states
- test stepper motion and track-zero strategy
- read write-protect state
- capture raw RDDATA timing
- verify SAFE/WRITE hardware interlock

## Phase 2 - RP2350 firmware

- USB device identification
- motor/enable control
- PH0-PH3 head stepping
- track seek/home commands
- read timing capture using RP2350 PIO
- WRDATA generation using PIO
- host-visible write-protect state
- bounded command timeouts and safe reset state

## Phase 3 - Sector I/O

- Apple 16-sector GCR decode/encode
- DOS 3.3 track/sector reads
- ProDOS block reads
- sector write/verify
- retry and bad-sector reporting

## Phase 4 - Host filesystem layer

### Linux

- FUSE filesystem
- `/media/appleii` mount
- DOS 3.3 read/write file operations
- ProDOS read/write directories and files
- Apple file type / aux type extended attributes

### Windows

- WinFsp filesystem
- Explorer-visible drive letter
- DOS 3.3 and ProDOS operations
- Apple metadata preservation

## Phase 5 - Preservation features

- `.dsk`, `.do`, `.po` imaging
- `.nib` support
- `.woz` read/write where practical
- raw timing/flux-oriented capture
- half/quarter-track experiments
- protected-disk analysis tools
