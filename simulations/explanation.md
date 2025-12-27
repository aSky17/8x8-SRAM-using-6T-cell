## Read and Write Operation Waveforms

### Read and Write ‘1’
This waveform illustrates a write-‘1’ operation followed by a read-‘1’ access. During the write phase, the write enable (WE) signal is asserted and the selected wordline is activated, allowing the write driver to force complementary data onto the bitlines and store logic ‘1’ in the addressed SRAM cell. During the read phase, WE is deasserted, the bitlines are precharged, and a small voltage differential develops based on the stored data, which is amplified by the sense amplifier to produce a full-swing output without disturbing the stored value.

### Read and Write ‘0’
This waveform illustrates a write-‘0’ operation followed by a read-‘0’ access. When WE is asserted, the write driver overpowers the pull-up devices of the 6T cell and pulls the appropriate bitline low to store logic ‘0’. During the read phase, the precharged bitlines develop an opposite differential compared to the read-‘1’ case, and the sense amplifier correctly resolves the stored ‘0’, confirming proper write and read functionality.
