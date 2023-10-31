# Remote Monitoring Dashboard

## Purpose
The purpose of this project is to construct a piece of software similar to that of MoTec's M1 Tune. It should communicate with the car to display real time data and to be able to update values within the VCU (two way communication). This is the UI/UX portion of the [[Remote Monitoring Firmware]] and the [[VCU WiFi Expansion Card]] projects.

## Functional Requirements (FR)
#### Communication
- Two way communication between laptop and VCU
- Real time
- Exact method of communication should be determined along with the team working on the [[Remote Monitoring Firmware]].
#### User Interface
- Should be designed to work on a desktop environment
- Display information in ways that best represent the type of information
	- Graphs and numerical values for speed, power draw,  ...
	- Dial encoder view for steering angle
	- text boxes and numerical values for control constants
- Ability to pause data/graphs would be AMAZING!
- Bonus points for including something scalable across multiple monitors

#### Data to be displayed
This should not be used as the full list but would be a good starting point. Refer to [[VCU Exposed Hardware]] for a full list of things that would be helpful to view. If undetermined, error on the side of yes over no.
- Wheel Speeds
- Motor Current Draw
- Battery Voltage
- Avg Cell Voltage
- Motor Power Draw (kW)
- Battey heat map (for voltage and temperature)
- Steering angle
- APPS and brake positions
- Internal VCU states
	- Scheduled tasks
	- Internal Faults
	- Raw Analog readings
- CAN bus messages
- System Faults

## Relevant Documents
- [[VCU WiFi Expansion Card]]
- [[VCU Exposed Hardware]]
- [[Remote Monitoring Firmware]]