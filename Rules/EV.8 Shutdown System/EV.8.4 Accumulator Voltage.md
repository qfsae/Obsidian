#### EV.8.4.1
The AMS must measure the cell voltage of every cell
- When cells are directly connected in parallel, only one voltage measurement is needed

#### EV.8.4.2
Cell Voltage levels must remain inside the allowed minimum and maximum cell voltage levels stated within the cell data sheet. Measurement accuracy must be considered

#### EV.8.4.3
All voltage sense wires connected to the AMS must meet one of:
- Have Overcurrent Protection [[#EV.8.4.4]]
- Meet the requirements for not having overcurrent protection listed within [[#EV.8.4.5]]

#### EV.8.4.4
When used, Overcurrent for the AMS voltage sense wires must meet the following:
- The overcurrent Protection must occur in the conductor, wire, or PCB trace which is directly connected to the cell tab
- The voltage rating of the Overcurrent Protection must be equal or greater than the smaller of:
	- The sum of the cell voltages sensed by the AMS board
	- The sum of the voltages sensed between galvanic isolation boundaries on the cell board/AMS

#### EV.8.4.5
Overcurrent Protection is not required on a voltage sense wire of all three of the following conditions are met:
- AMS is a distributed AMS system (one measurement per cell board)
- Sense wire length < 25 mm
- AMS board has over current protection
