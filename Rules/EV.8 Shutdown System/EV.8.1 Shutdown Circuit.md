#### EV.8.1.1
The [[EV.8.1 Shutdown Circuit|Shutdown Circuit]] must open when any of the following exist:
 - Operation of, or detection from any of the components listed (within EV.8.8.1):
	 - Accumulator Management System ([[EV.8.3 AMS|AMS]])
	 - Isolation Monitoring Device ([[EV.8.6 IMD|IMD]])
	 - Brake System Plausibility Device ([[EV.8.7 BSPD|BSPD]])
	 - High Voltage Interlocks ([[EV.8.8 Interlocks]])
	 - Master Switches ([[EV.8.9 Master Switches]])
	 - Shutdown Buttons ([[EV.8.10 Shutdown Buttons]])
	 - Brake Over Travel Switch ([[T.3 Braking System|BOTS]])
	 - Inertia Switch ([[T.9 Electrical Equipment#T.9.4 Inertia Switch]])
- The [[EV.8.1 Shutdown Circuit|Shutdown Circuit]] must carry the current driving the [[EV.6.4 Accumulator Isolation Relays|AIR]]s and the [[EV.6.6 Precharge and Discharge|Precharge Circuit]] relay
#### EV.8.1.3
The [[EV.8.3 AMS|AMS]], [[EV.8.6 IMD|IMD]], and [[EV.8.7 BSPD|BSPD]] must be normally open
#### EV.8.1.4
The The [[EV.8.3 AMS|AMS]], [[EV.8.6 IMD|IMD]], and [[EV.8.7 BSPD|BSPD]] must be completely independent and not be able to feed power back into the shutdown circuit
#### EV.8.1.5
The [[EV.8.10 Shutdown Buttons]], [[T.3 Braking System]], TSMS, GLVMS [[EV.8.9 Master Switches]], and Interlocks must directly carry the current of the shutdown circuit (no relays)
#### EV.8.1.6
Teams must be able to demonstrate functionality of shutdown circuit at technical inspection
#### EV.8.2.2
When the [[EV.8.1 Shutdown Circuit]] opens:
- The Tractive System must shutdown
- All Accumulator current flow must stop immediately
- The voltage in the tractive system must be [[T.9 Electrical Equipment#T.9.2 Low Voltage Batteries]] in 5 seconds or less
- The motors must spin free. Torque must not be applied to the motor
#### EV.8.2.3
When the [[EV.8.3 AMS]], [[EV.8.6 IMD]], or [[EV.8.7 BSPD]] open the shutdown circuit:
- the tractive system must remain disabled until manually reset
- the driver must not be able to reactivate the system from within the car
- operation of the [[EV.8.10 Shutdown Buttons]] or TSMS [[EV.8.9 Master Switches]] must not reset the shutdown circuit
- reset must only be possible by a manual action of a person directly at the vehicle (LVMS)


![[Shutdown Circuit Diagram.png]]

## Precharge
- Cascadia Inverter supplies relay power for precharge circuit through RLY1
	- Also supplies power for main contactor relay (not used)
	- see page 54 of manual
