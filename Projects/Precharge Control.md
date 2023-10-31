# Precharge Control
## Purpose
The purpose of the precharge circuit is limit the inrush current to the Inverter's capacitors. Precharge circuitry generally consists of a a relay connected to a resistor that bypasses the positive isolation relay.

The precharge controller circuit controls when the second [[EV.6.4 Accumulator Isolation Relays|AIR]] closes. The [[Cascadia CM200DX]] contains a low side controller. This controller must be examined for rules compliancy. If it is rules compliant, then the correct wiring must be added into the Accumulator and Inverter harnesses to accommodate this feature. The correct software logic must also be instantiated.

If the CM200DX precharge circuitry is insufficient, then a delay or voltage based precharge controller PCB will need to be developed. See [[EV.6.6 Precharge and Discharge]] for more information.  Rules recommends >95% charge before release, but the higher charge on the capacitors the less risk is involved. Subsequently, the capacitors will also last longer.

## Relevant Documents
- [How to design a precharge circuit](https://www.sensata.com/sites/default/files/a/sensata-how-to-design-precharge-circuits-evs-whitepaper.pdf)
- [[PM CM and RM Hardware User's Manual (V3_7) (1).pdf]]
- [[Cascadia CM200DX]]
## Rules
- [[EV.6.6 Precharge and Discharge]]
- [[Shutdown Circuit Diagram.png]]
- [[EV.8.1 Shutdown Circuit]]