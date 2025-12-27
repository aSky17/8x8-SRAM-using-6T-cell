# Transistor Sizing and Stability Considerations

Proper transistor sizing is critical to ensure SRAM stability, write-ability, and reliable read operation.

## 6T Cell Sizing
- Pull-down NMOS devices are sized stronger than access transistors to prevent read disturb.
- Access transistors are sized to balance read stability and write-ability.
- Pull-up PMOS devices are intentionally weaker so that the write driver can successfully overwrite the stored data.

This sizing ensures:
- Read Stability: Stored data is not flipped during a read operation.
- Write Margin: New data can be written reliably.

## Static Noise Margin (SNM)
Static Noise Margin is used as a metric to evaluate cell stability.
- SNM is extracted using the butterfly curve method.
- Both Hold SNM (HSNM) and Read SNM (RSNM) are analyzed.

A higher SNM indicates better immunity to noise and process variations.

## Peripheral Circuit Considerations
- Write drivers are sized to overpower the pull-up PMOS devices in the cell.
- Sense amplifiers are designed to detect very small bitline differentials.
- Precharge transistors are sized to ensure fast and symmetric bitline charging.
