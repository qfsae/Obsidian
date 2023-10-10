## T.4.1 Applicability
This section applies to:
- IC vehicles using Electronic Throttle Control (ETC)
- EV

## T.4.2 Accelerator Pedal Position Sensor (APPS)
#### T.4.2.1
The APPS must be actuated by a foot pedal
- Pedal travel is defined as a percent travel from a fully release position to a fully applied position where 0% is released and 100% is fully applied
- The foot pedal must return to its original position when not actuated
- The foot pedal must have a positive stop preventing APPS from damaged or overstressed
- Two springs must be used to return the foot pedal to the OFF position
- Each spring must be capable of returning the pedal to the fully released position with the other disconnected
- The springs in the APPS are not acceptable pedal return springs

#### T.4.2.2
Two or more electrically separate sensors must be used as APPSs. A single OEM type APPS with two completely separate sensors in a single housing is acceptable

#### T.4.2.3
The APPS sensors must have different transfer functions which meet one of:
- Each sensor has a positive slope sense with different gradients and/or offsets to the other(s)
- An OEM pedal sensor with opposite slopes
	- Non OEM opposite slope sensor configurations require prior approval
The intent is that in a short circuit the APPS will only agree at 0% pedal position

#### T.4.2.4 Implausibility
Implausibility is defined as a deviation of more than 10% pedal travel between the sensors or other failure as defined within [[#T.4.2 Accelerator Pedal Position Sensor (APPS)]]. Use of values larger than 10% require justification in the FMEA and may not be approved

#### T.4.2.5 Fault Detection
If an implausibility occurs between the values of the APPS and persists for more than 100 msec, the power to the Motors must be stopped immediately
EV - It is not necessary to open the [[EV.8.1 Shutdown Circuit]], the motor controllers stopping power to the motor is sufficient.

#### T.4.2.6 Use of 3 Sensors
If three sensors are used, best two of three algorithms can be utilized. See rules for more information.

#### T.4.2.7 Testing
Each APPS must be able to be checked during [[IN.4 Electrical Technical Inspection]] by having one of:
- A separate detachable connector that enables a check of the functions by unplugging it
- An inline switchable breakout box available that allows disconnection of each APPS signal

#### T.4.2.8 Transmission
The APPS signals must be sent directly to a controller using an analogue signal or via a digital data transmission bus such as CAN or FlexRay

#### T.4.2.9
Any failure of the APPS or APPS wiring must be detectable by the controller and must be treated like an [[#T.4.2.4 Implausibility]]

#### T.4.2.10 Analogue Signaling
When an analogue signal is used, the APPS will be considered to have failed when they achieve an open/short circuit condition which generates a signal outside the operating range. For example:
- <0.5V or >4.5V
- The circuitry used to evaluate the sensor must use pull down or pull up resistors to ensure that open circuit signals result in a failure being detected.

#### T.4.2.11 Digital Signaling
When any kind of digital data transmission is used to transmit the APPS signal,
- The FMEA study must contain a detailed description of all the potential failure modes that can occur, the strategy that is used to detect these failures and the tests that have been conducted to prove that the detection strategy works.
- The failures to be considered must include but are not limited to the failure of the APPS, APPS signals being out of range, corruption of the message and loss of messages and the associated time outs

#### T.4.2.12
The rules stated within [[#T.4.2 Accelerator Pedal Position Sensor (APPS)]] apply only to the APPS (pedal) signals. However, the integrity of the torque command signal must also be considered


## T.4.3 Brake System Encoder (BSE)
#### T.4.3.1
The vehicle must have a sensor or switch to measure brake pedal position or brake system pressure

#### T.4.3.2
The BSE must be able to be checked during technical inspection by having one of:
- A separate detachable connection to the ECU without affecting any other connections
- An inline switchable breakout box that allows disconnection of each BSE signal to the main ECU without affecting any other connections

#### T.4.3.3
The BSE or switch signals must be sent directly to a controller using an analogue signal or via a digital data transmission bus such as CAN or FlexRay
Any failure of the BSE or BSE wiring that persists more than 100 msec must be detectable by the controller and treated like an implausibility and power to the (IC) electronic throttle / (EV) Motor(s) must be immediately stopped completely.
(EV only) It is not necessary to completely deactivate the Tractive System, the motor controller(s) stopping power to the motor(s) is sufficient.

#### T.4.3.4
When an analogue signal is used, the BSE sensors will be considered to have failed when they achieve an open circuit or short circuit condition which generates a signal outside of the normal operating range, for example <0.5 V or >4.5 V.
The circuitry used to evaluate the sensor must use pull down or pull up resistors to ensure that open circuit signals result in a failure being detected.

#### T.4.3.5
When any kind of digital data transmission is used to transmit the BSE signal:
- The FMEA study must contain a detailed description of all the potential failure modes that can occur, the strategy that is used to detect these failures and the tests that have been conducted to prove that the detection strategy works. 
- The failures modes must include but are not limited to the failure of the sensor, sensor signals being out of range, corruption of the message and loss of messages and the associated time outs.
- In all cases a sensor failure must immediately shutdown power to the motor(s).