List of all parts associated with the HV (High Voltage) System

## Accumulator Parts
#### Parts directly pertaining to the [[EV.8.1 Shutdown Circuit]]
- [[EV.8.3 AMS]]
	- [[Orion 2 BMS]] - Measures cell voltages, current protection, fuse protection
		- Page 64 [[orionbms2_wiring_manual.pdf]] -> all cell taps are fused
		- 10 Cell groups with 10 cells each
		- 100V isolation between Cell groups (page 60 [[orionbms2_wiring_manual.pdf]])
	- [[Temp Monitor PCB]] - measures [[EV.8.5 Accumulator Temperature]]
- [[Isolation Relays]]
- [[IMD Ordering]] / [[EV.8.6 IMD]]
- Accumulator to Inverter Connector
	- Must adhere to [[EV.6.10 TS Connectors]]
#### Other Parts (may include [[EV.8.8 Interlocks]])
- [[Sony VTC6]] batteries from [[Sony VTC6|Enepaq]]
	- See also bus bars and screw terminals from [[Sony VTC6|Enepaq]]
	- 100s6p config -> 6 segments
		- $18*4.2V_{DC}=84V_{DC}$
		- $20*3.6V_{DC}=72V_{DC}$
		- $20*2.5V_{DC}=50V_{DC}$
	- Segments must adhere to [[EV.6.1 Energy Storage]] (EV.6.1.2)
		- $64.8Wh*20*3.6V-{DC}=4.665 MJ$
		- 20s6p -> 4.66 MJ
	- Segments must be isolated according to [[EV.7.2 Insulation]]
- [[EV.4 Electrical Limitations#EV.4.3 Energy Meter]]
	- Placed outside of the Accumulator?
	- Must be easily assessable
- [[Maintenance Plugs]] - for [[EV.6.3 Maintenance Plugs]]
	- Used to separate Accumulator Segments
- [[EV.6.5 High Voltage Disconnect]]
	- Placed inline with [[EV.4 Electrical Limitations#EV.4.3 Energy Meter|Energy Meter]]?
	- placed outside of Accumulator
	- Have to find a suitable Connector -> [[HVD Research]]
	- Has to include [[EV.8.8 Interlocks]]
- [[EV.6.6 Precharge and Discharge]]
	- Precharge
		- [[Cascadia CM200DX Ordering]] -> See precharge components offered by Cascadia
		- Inverter will control low side of second AIR
			- High side has to be supplied from [[EV.8.1 Shutdown Circuit]] -> [[Shutdown Circuit Diagram.png]]
		- Precharge relay will be directly connected to [[EV.8.1 Shutdown Circuit]]
	- Discharge
		- [[Inverter Discharge Process (V0_9).pdf]] -> Inverter Discharge not Rules Compliant -> Discharge Circuit needed
		- [[Discharge Circuit]]
		- Must be able to discharge inverter when [[EV.8.1 Shutdown Circuit]] or [[EV.6.5 High Voltage Disconnect]] is disengaged
- [[EV.6.7 Voltage Indicator]] -> Part of [[Accumulator Indication Panel]]
	- Placed on outside of Accumulator Container
	- powered by [[Voltage Indicator PCB]]
	- Draws power directly from TS
- Inverter/Charger Power Connection(s)
	- Must follow [[EV.6.10 TS Connectors]]
	- Research on connectors that include an interlock -> [[TS Connectors]]
- Accumulator Wiring
	- Must follow [[EV.7.3 Wiring]]
	- Low Current Wiring -> follows:
		- [[GLV Connectors]]
		- [[HV Wiring]]
	- High Current Wiring -> follows:
		- [[EV.7.4 Connections]]
		- [[HV Wiring]]
	- GLV supply wiring must follow [[EV.7.5 Voltage Separation]]
- Isolated CAN bus for [[EV.7.5 Voltage Separation#EV.7.5.9]]


## Tractive System
#### Inverter/Motor Controller
- [[Cascadia CM200DX]] -> 225kW Inverter
- [[Cascadia CM200DX Ordering]]

#### Motor
- [[Emrax 188HV]]

#### Wiring
- [[Cascadia CM200DX Ordering]] From Cascadia includes connection cables for connecting motor and inverter side of Accumulator->Inverter Connection


## Charging
- TBD [[Charging Research]]