## EV.4.1 Power and Voltage
- The maximum power drawn from the Accumulator must not exceed 80kW
- The maximum voltage between any two points may not exceed 600VDC
- The powertrain must not regenerate energy between 0 and 5 km/h
## EV.4.2 Operation
- Supplying power to the motor to drive the wheel in reverse is prohibited
- drive by wire control of wheel toque is permitted
- any algorithm or ECU that can adjust the requested wheel torque must only lower the total driver requested torque and must NOT increase it.
## EV.4.3 Energy Meter
- EV.4.3.1 All Electric Vehicles must run with the energy meter provided by the event organizer
	- refer to the <a href="https://fsaeonline.com/cdsweb/gen/DownloadDocument.aspx?DocumentID=96d652ca-a506-444e-917a-dbf695321ab3#%5B%7B%22num%22%3A36%2C%22gen%22%3A0%7D%2C%7B%22name%22%3A%22XYZ%22%7D%2C69%2C367%2C0%5D">FSAE website</a> for more information
- EV.4.3.2 The Energy Meter must be installed in an easily assessable location
- EV.4.3.3 All power supplying the TS must flow through the Energy Meter
- EV.3.4 Power and Voltage limits will be checked by the Energy Meter data
- Energy Meter Specifications found from <a href="https://fsaeonline.com/content/Energy-Meter-Specification-021317.pdf">FSAE EM Documentation</a>:
	- Placed Inline with HV Bus bar supply and Accumulator
		- *Note* Looks more like it should be placed between AIRs and Inverter
		- https://www.reddit.com/r/FSAE/comments/7851tm/energy_meter_placement/
	- data lines must be available to competition organizers from outside of TS enclosure
	- teams responsible for supplying mating connector (MOLEX part number)
	- 600A max cont. current

## EV.4.4 Violations
- EV.4.4.1 A Violation occurs:
	- When one or two of the following exist:
		- Use of more than the maximum power
		- Exceed the maximum voltage
	- For one or both conditions:
		- Continuously for 100 ms or more
		- After a moving average of 500 ms is applied
- Missing energy meter due to the teams fault, tampering, or attempting to tamper with the energy meter will be treated as a violation
- Tampering or attempting to tamper with the [[#EV.4.3 Energy Meter]] or its data may result in a Disqualification (DQ)