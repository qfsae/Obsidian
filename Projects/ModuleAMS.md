# ModuleAMS
Modular AMS that sits between two battery cells, using the potential between the negative terminal on cell A and the positive terminal on cell B to power itself while measuring the potential difference between the two terminals of cell A. A low power microcontroller is used to collect the cell voltage measurements and temperature measurements.

Further isolation could be achieved on the device by finding a microcontroller with an operating voltage below 3V and removing the tap onto cell B.

This board would replace the BMS and Temp monitor board. It would require the BMS to be in the charger, operating similar to a drone battery. This runs the risk of not being able to utilize the full capacity of the cells. (assuming that internal resistances differ).

#### Evaluation
Further research on cell balancing, rules and lp microcontrolers would be required to determine the viability of this project. IR of cells needs to be known. 

#### Sources
https://www.ti.com/download/trng/docs/seminar/Topic%202%20-%20Battery%20Cell%20Balancing%20-%20What%20to%20Balance%20and%20How.pdf