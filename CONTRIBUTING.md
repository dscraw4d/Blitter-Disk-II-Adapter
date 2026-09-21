# Contributing

Hardware review, measurements, documentation fixes, firmware work, and host-software contributions are welcome.

## Please do not silently change safety-critical wiring

Changes involving any of the following should be proposed in an issue first and include a technical reason:

- +12 V, +5 V or -12 V generation
- Disk II 20-pin mapping
- output-enable defaults
- write-request gating
- logic-level translation
- grounding
- current protection

## Hardware test reports

Useful reports include:

- exact board/module part numbers
- measured rail voltages
- logic-analyzer or oscilloscope captures
- Disk II model/revision
- Apple media type tested
- read/write results
- photos of the prototype wiring

Do not describe Rev B as production-ready solely because one prototype works. Repeatable validation matters.

## Credit

Please retain:

**Project conceived and directed by Darren Crawford (Viper).**
