# Vehicle Control Unit
## Purpose
The VCU (Vehicle Control Unit) is the replacement for the MoTec ECU previously used in the teams IC cars. 
It serves as both the GLV power distribution network, similar to MoTec's PDM, and as the main control unit for the car.

In addition to controlling the motor and providing LV power to the car, the VCU is also responsible for numerous rules safety and plausibility checks.

### Technical Requirements
- ADC - Analog to Digital Conversions
	- Steering
	- Throttle Pedals
	- Brake Pedals
	- Temperature Sensors
- DSP - Digital Signal Processing
	- Wheel Speed Sensors (PWM)
- Communications
	- 2x CAN Bus Interfaces
		- [[Orion 2 BMS]]
		- [[Cascadia CM200DX]]
	- I2C Ride Height Sensors (*double check with aero*)
- Power
	- Cooling Pump Control (24V)
	- Sensors Power
		- Steering (12V)
		- Throttle Pedals (5V)
		- Brake (12V)
		- Temp Sensors (12V)
		- Wheel Speed (12V)
		- Suspension LinPots (12V)
	- Data Logger (24V)
	- BMS (12V)
	- Accumulator Temperature Monitor
	- [[Cascadia CM200DX]] Inverters (24V)
	- [[EV.6.4 Accumulator Isolation Relays|Isolation Relays]] (12V)
	- Dashboard (24V)
	- Safety Lights


## Rules
- [[EV.5.7 APPS & Brake Plausibility Check]]
- [[EV.5.4 Grounded Low Voltage System]]
- [[T.9 Electrical Equipment]]

## Relevant Documents
- [[Orion 2 BMS]]
- [[Temp Monitor PCB]]
- [[CAN bus]]
- [[CAN Protocol (V6_2).pdf]]
- [[CAN bus general info]]
- [[Dashboard]]
- [[Dashboard CAN Protocol]]