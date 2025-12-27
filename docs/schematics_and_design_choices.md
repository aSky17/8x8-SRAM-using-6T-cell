# Schematic Design and Circuit Choices

This document explains the rationale behind the schematic-level design decisions used in the SRAM.

## Choice of 6T SRAM Cell
The traditional 6T SRAM cell was selected due to:
- Proven robustness and widespread industry use
- Simple differential read and write mechanism
- Good balance between stability, area, and performance

## Row Decoder Design
- Implemented using NAND gates followed by inverters.
- Ensures only one wordline is active at a time.
- Active-high wordline simplifies access transistor control.

## Column Decoder and Multiplexer
- A 3-to-8 column decoder generates column select signals.
- Transmission-gate-based 8-to-1 MUX minimizes signal degradation.
- Differential routing preserves noise immunity.

## Precharge and Equalization Circuit
- Both bitlines are precharged to VDD before read.
- Equalization ensures BL and BL̅ start at the same voltage.
- This improves sensing accuracy and reduces offset errors.

## Sense Amplifier Choice
- A latch-type differential sense amplifier was used.
- Capable of amplifying very small voltage differences.
- Provides fast sensing with low static power consumption.

## Write Driver Design
- Differential write driver drives complementary data.
- Designed to overpower the cell’s pull-up devices during write.
- Ensures reliable write operation across all cells.
