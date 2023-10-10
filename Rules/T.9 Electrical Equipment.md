## T.9.1 Definitions
- T.9.1.1 High Voltage - HV
	- any voltage greater than 60 VDC or 25V AC RMS
- T.9.1.2 Low Voltage - LV
	- Any voltage below and including 60 VDC and 25 AC RMS
- T.9.1.3 Normally Open
	- A type of electrical relay or contactor that allows current flow only in the energized state

## T.9.2 Low Voltage Batteries
- T.9.2.1 All Low Voltage Batteries and onboard power supplies must be attached securely to the Chassis
- T.9.2.2 All Low Voltage Batteries must have Overcurrent protection that trips at or below the maximum specified discharge current of the cells
- T.9.2.3 The hot (ungrounded) terminal must be insulated
- T.9.2.4 Any wet cell battery located in the driver compartment must be enclosed in a nonconductive marine type container or equivalent
- T.9.2.5 Batteries or battery packs based on lithium chemistry must meet of the two:
	- Have a rigid, sturdy casing made from nonflammable material
	- A commercially available battery designed as an OEM style replacement
- T.9.2.6 All batteries using chemistries other than lead acid must be presented at Technical Inspection with markings identifying it for comparison to a datasheet or other documentation proving the pack and supporting electronics meet all rules requirements

## T.9.3 Master Switches
Each Master switch ( IC.9.3 /  [[EV.8.9 Master Switches]] ) must meet the following:
### T.9.3.1 Master Switch Location
- On the driver's right hand side of the vehicle
- In proximity to the Main Hoop
- At the driver's shoulder height
- Able to be easily actuated from outside the vehicle

### T.9.3.1 Master Switch Characteristics
- Be of the rotary mechanical type
- Be rigidly mounted to the vehicle and must not be removed during maintenance
- Mounted where the rotary axis of the key is near horizontal and across the vehicle
- The ON position must be in the horizontal position and marked accordingly
- The OFF position must be clearly marked
- (EV only) Operated with a red removable key that must only be removable in the electrically open (OFF) position

## T.9.4 Inertia Switch
- T.9.4.1 Inertia Switch Requirement
	- EV Must have an Inertia Switch
	- IC Should have an Inertia Switch
- T.9.4.2 The Inertia Switch must be:
	- A Sensata Resettable Crash Sensor or equivalent
	- Mechanically and rigidly attached to the vehicle
	- Removable to test functionality
- T.9.4.3 Inertia Switch Operation
	- Must trigger due to an impact load which decelerates the vehicle between 8 g and 11 g depending on the duration of the deceleration
		- Refer to the spec sheet of the Sensata device
	- Must open the [[EV.8.1 Shutdown Circuit]] if triggered
	- Must latch until manually reset
	- May be reset by the driver from inside the driver's cell
