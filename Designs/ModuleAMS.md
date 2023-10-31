# ModuleAMS
## Design 1: Current Bypass
Modular AMS design that sits between two battery cells, using the potential between the negative terminal on cell A and the positive terminal on cell B to power itself while measuring the potential difference between the two terminals of cell A. A low power microcontroller is used to collect the cell voltage measurements and temperature measurements.

Further isolation could be achieved on the device by finding a microcontroller with an operating voltage below 3V and removing the tap onto cell B.

This board would replace the BMS and Temp monitor board.

### Balancing Capabilities
The Current Bypass balancing method utilizes a controller switch along with a dissipation resistor to dissipate extra energy stored in the monitored cell in the form of heat. The main goal of this balancing device is to prevent overcharging of cells during charging.

### Analysis
#### Benefits
- Modular BMS means less packaging constraints than with centralized unit
- Easier to achieve isolation requirements set out in FSAE Rules
- Easier to achieve fusing requirements set out in FSAE Rules
- Singular device used for temperature and voltage monitoring reduces overall complexity of design
- Low component/Design complexity
- Simple programming complexity
#### Drawbacks
- 0% Efficiency 
	- Cannot be used while driving
	- Does not increase/extend usable energy in cells
- Large thermal dissipation

#### Evaluation
Due to the simplicity of the device, it would be a good last choice for a team looking for simple balancing on a budget. However, the device does not contain any means of extending the usable life of the battery, therefore if the internal resistances of cells are nonuniform or are largely deviated, this design would be fatal in terms of battery lifetime. Overall this design is not recommended.

## Design 2: Charge Redistribution 
This design would consist of modules that each span a group of series cells. The best option for this design would be for a module to span an entire battery segment. The design consists of switching devices along with capacitors for charge redistribution. It works through the principle of potential imbalances between cells. By first connecting a capacitor to the cell with higher potential, and then to the cell with lower potential, charge is transferred through the capacitor from the cell with higher charge to the cell with lower charge. Switchable networks can be added to redistribute charge over longer distances, although the increase in complexity may not warrant the benefits.

### Balancing Capabilities
Because this design uses capacitors to redistribute charge, it is significantly more efficient than the current bypass method. The main goal of this design is to extend the usable energy of the battery by transferring energy from cells with lower internal resistances to those with higher IR. However this design is significantly more complex and requires a higher understanding of cell balancing in order to write the balancing algorithm required for its operation.v

### Analysis
#### Benefits
- Being integrated into the battery segments simplifies packaging
- Easier to achieve isolation requirements set out in FSAE Rules
- Easier to achieve fusing requirements set out in FSAE Rules
- Supports charge redistribution 
#### Drawbacks
- Technically complex
	- Electrically and Software
- Large R&D Time

#### Evaluation
This would be the recommended method for teams trying to implement a custom BMS. Still, it remains much more complex than an off the shelf unit


#### Sources
https://www.ti.com/download/trng/docs/seminar/Topic%202%20-%20Battery%20Cell%20Balancing%20-%20What%20to%20Balance%20and%20How.pdf