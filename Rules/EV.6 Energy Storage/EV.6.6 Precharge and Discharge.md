#### EV.6.6.1 Precharge Circuit
The Accumulator must contain a Precharge Circuit. The Precharge Circuit must:
- Be able to charge the Intermediate Circuit (Inverter Capacitors) to a minimum of 90% (>95% recommended) before closing the second [[EV.6.4 Accumulator Isolation Relays|AIR]] 
- Be supplied from the [[EV.8.1 Shutdown Circuit]]
- Not be fused

#### EV.6.6.2 Precharge Control
- The intermediate Circuit (Inverter) must precharge before closing the second AIR.
- The end of the precharge must be controlled by one of the two following options:
	- Feedback by monitoring the voltage in the Intermediate Circuit
	- A conservative time defined by the longer of:
		- Twice the time to charge to 90%
		- The time to charge to 90% plus 500 ms

#### EV.6.6.3 Discharge Circuit
The Tractive System must contain a Discharge Circuit. The Discharge Circuit must be:
- Wired in a way that it is always active when the [[EV.8.1 Shutdown Circuit]] is open
- Able to discharge the Intermediate Circuit (Inverter Capacitors) if the [[EV.6.5 High Voltage Disconnect]] has been opened
- Not be fused
- Designed to handle the maximum discharge Current for a minimum of 15 seconds

EV.6.6.4 Positive Temperature Coefficient (PTC) devices must not be used to limit current for the Precharge or Discharge Circuits

EV.6.6.5 The Precharge relay must be a mechanical type relay