# Windows / Linux Host Software

**Status: planned - not implemented in Revision B.**

The target host stack is:

```text
USB transport
     |
Disk II sector / timing layer
     |
DOS 3.3 + ProDOS filesystem library
     |
+-------------------+
|                   |
WinFsp              FUSE
Windows             Linux
```

Planned features:

- detect connected Blitter Disk II Adapter
- identify inserted DOS 3.3 or ProDOS floppy
- cache catalog/directory and allocation structures
- mount read/write as a Windows drive letter or Linux mount point
- preserve ProDOS file type and auxiliary type
- expose write-protect state
- safe flush/eject
- optional disk-image creation and restoration

DOS 3.3 should remain a flat directory. ProDOS can expose real subdirectories.
