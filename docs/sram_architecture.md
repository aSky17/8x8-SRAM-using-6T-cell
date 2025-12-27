# SRAM Architecture Overview

This project implements a transistor-level 8×8 Static Random Access Memory (SRAM) array designed in Cadence Virtuoso. The architecture follows a conventional SRAM organization, separating the design into an address path and a data path for modularity and scalability.

## Array Organization
- Memory Size: 8 × 8 (64 bits)
- Storage Element: Traditional differential 6T SRAM cell
- Organization: 8 rows × 8 columns

Each row is selected using a row decoder, while column selection and data routing are handled through a column decoder and multiplexer.

## Address Path
- A 3-to-8 row decoder activates exactly one wordline (WL0–WL7).
- A 3-to-8 column decoder generates column select signals.
- An 8-to-1 transmission-gate-based column multiplexer connects the selected column to the global data bus.

## Data Path
- Bitlines (BL/BL̅) are precharged and equalized before every access.
- During write, a differential write driver forces data onto the bitlines.
- During read, a latch-type differential sense amplifier amplifies the small voltage difference on the bitlines to full-swing digital levels.

## Scalability
The modular nature of the decoders, bitline circuitry, and sense amplifier allows the architecture to be extended to larger arrays (e.g., 32×32 or 64×64) without major structural changes.
