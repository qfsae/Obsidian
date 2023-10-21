#### EV.8.3.1
An Accumulator Management System must monitor the e [[EV.8.4 Accumulator Voltage]] and [[EV.8.5 Accumulator Temperature]] when the:
- Tractive System is Active [[EV.10 Vehicle Operations]]
- Accumulator is connected to a Charger [[EV.9 Charging]]

#### EV.8.3.2
The AMS must have galvanic isolation at every segment to segment boundary, as approved in the ESF

#### EV.8.3.3
Cell balancing is not permitted when the [[EV.8.1 Shutdown Circuit]] is open [[EV.9.3 Charging Shutdown Circuit]]

#### EV.8.3.4
The AMS must monitor for:
- Voltage values outside the allowable range [[EV.8.4 Accumulator Voltage#EV.8.4.2]]
- Voltage sense [[EV.7.6 Overcurrent Protection]] devices blown or tripped
- [[EV.8.5 Accumulator Temperature]] values outside the allowable range
- A missing or interrupted voltage or temperature measurements
- A fault within the AMS

#### EV.8.3.5
If the AMS detects one or more of the conditioned mentioned within [[#EV.8.3.4]], the AMS must:
- Open the [[EV.8.1 Shutdown Circuit]]
- Turn on the [[#EV.8.3.6 Indicator Light]]
	- The light must stay on until the AMS is reset

#### EV.8.3.6 Indicator Light
The AMS Indicator Light must be:
- Color: Red
- Clearly visible to the seated driver in bright sunlight
- Clearly marked with the lettering "AMS"