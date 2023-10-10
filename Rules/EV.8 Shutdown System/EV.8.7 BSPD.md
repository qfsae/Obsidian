# EV.8.7 Brake System Plausibility Device - BSPD

#### EV.8.7.1
The vehicle must have a standalone nonprogrammable circuit to check for simultaneous braking and high power output
The BSPD must be provided in addition to the [[EV.5.7 APPS & Brake Plausibility Check]]

#### EV.8.7.2
The BSPD must open the [[EV.8.1 Shutdown Circuit]] when the two of these exist:
- Demand for hard braking [[T.4 ETC Components]] 
- Motor/Accumulator current is at a level were 5kW of electrical power in the DC circuit is delivered to the motor(s) at nominal voltage
The BSPD may delay opening the shutdown circuit up to 0.5 seconds to avoid false trips

#### EV.8.7.3
The BSPD must open the [[EV.8.1 Shutdown Circuit]] when there is an open circuit or short in any sensor input
#### EV.8.7.4 Demonstration
The team must have a test to demonstrate BSPD operation at [[IN.4 Electrical Technical Inspection]]
- Power must not be sent to motors during test
- Test must prove the function of the complete BSPD in the vehicle, including the current sensor