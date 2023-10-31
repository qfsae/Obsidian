# Vehicle Control Unit
## Purpose
The VCU is the replacement for the MoTec ECU previously used in the teams IC cars. It serves as both the GLV power distribution network, similar to MoTec's PDM, and as the "brains" of the car.

This is the teams first major firmware project, involving all aspects of programming from writing interface drivers for the ARM chip's peripherals to writing the torque control logic for the motor.

In addition to controlling the motor and providing LV power to the car, the VCU is also responsible for numerous rules safety and plausibility checks.

Further information will be available on the VCU shortly. Currently, the V0.0 prototype is undergoing design review will be manufactured shortly. In the meantime, there are several firmware projects that can be completed on STM32 ARM development boards. A short list of some of the things required on the VCU is shown below:
- Wheel Speed PWM decoding
- Filesystem Implementation / Management
- Timer Interrupts
- CAN Bus Drivers/Interrupts
- Live Telemetry
	- ESP32 WiFi Driver
	- Telemetry Dashboard (Remote Program)
	- ESP32 WiFi Data Transmission
- ADC Drivers/Interrupts
- Motor Torque/Speed Controller
	- Traction Control
	- Acceleration Control
	- Regeneration Braking
- Brake Pressure Device Drivers (Analog Conversion)
- Throttle Pedal Device Drivers (Analog Conversion)
- Emergency Fault Handling
- RTOS Scheduling
- CAN Bus Device Drivers
	- Cascadia CM200DX
	- Orion 2 BMS
	- Temperature Monitor
	- Dashboard
- Lots and Lots of OS programming + Many More Projects (Including Integration)

## Rules
- [[EV.5.7 APPS & Brake Plausibility Check]]
- [[EV.5.4 Grounded Low Voltage System]]
- [[T.9 Electrical Equipment]]

## Relevant Documents
- [[Orion 2 BMS]]
- [[Temp Monitor Board]]
- [[CAN bus]]
- [[CAN Protocol (V6_2).pdf]]
- [[CAN bus general info]]
- [[Dashboard]]
- [[Dashboard CAN Protocol]]