# 8×8 Traditional 6T CMOS SRAM Design in Cadence Virtuoso

This project presents the design and functional verification of a transistor-level 8×8 SRAM array implemented using traditional 6T CMOS cells in 90 nm GPDK technology. The design includes complete peripheral circuitry and was verified using Spectre simulations in Cadence Virtuoso.

## Architecture
- 6T SRAM Cell (64 cells)
- 3-to-8 Row Decoder
- 3-to-8 Column Decoder with 8-to-1 Column MUX
- Bitline Precharge & Equalization Circuit
- Differential Write Driver
- Latch-Type Differential Sense Amplifier

## Technology & Tools
- Technology: GPDK 90 nm
- Tools: Cadence Virtuoso, Spectre, ADE

## Verification
- Read, Write, and Hold Operations
- Transient Simulation
- Static Noise Margin (SNM) Analysis

## Notes
Cadence databases and PDK files are not included due to licensing restrictions.
