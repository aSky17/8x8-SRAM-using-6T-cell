# Read and Write Operation

This document explains the functional operation of the SRAM during write, read, and hold modes.

## Write Operation
1. The desired row and column addresses are applied.
2. The row decoder asserts the selected wordline.
3. The write enable (WE) signal activates the differential write driver.
4. Complementary data (Din and Din̅) is driven onto BL and BL̅.
5. The write driver overpowers the pull-up PMOS devices in the 6T cell, forcing the cell to store the new value.

## Read Operation
1. Bitlines are first precharged and equalized.
2. The selected wordline is asserted while write enable remains disabled.
3. Depending on the stored data, one bitline discharges slightly.
4. A small differential voltage develops between BL and BL̅.
5. The sense enable (SE) signal activates the latch-type sense amplifier, converting the small differential signal into a full-swing digital output.

## Hold Operation
- Wordlines remain deasserted.
- The cross-coupled inverters inside the 6T cell retain the stored data.
- No bitline activity occurs, ensuring low static power consumption.
