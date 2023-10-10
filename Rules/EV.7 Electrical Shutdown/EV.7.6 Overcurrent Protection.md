#### EV.7.6.1
All Electrical systems (TS and GLV) must have appropriate Overcurrent Protection / Fusing

#### EV.7.7.2
Unless otherwise allowed within the rules, all Overcurrent Protection devices must:
- Be rated for the highest voltage in the systems they protect
- Overcurrent protection devices used form DC must be rated for DC and must carry a DC rating equal to or greater than the system voltage
- Have a Continuous Current rating less than or equal to the current rating of any electrical components that it protects
- Hand an interrupt current rating higher than the theoretical short current of the system that it protects

#### EV.7.6.3
Each parallel element of multiple parallel battery cells, capacitors, strings of battery cells, strings of capacitors, or conductors must have individual Overcurrent protection

#### EV.7.6.4
Any conductors (wires, busbars) conducting the entire pack current must meet one of:
- Be appropriately sized for the total current that the individual Overcurrent Protection devices could transmit
- contain additional Overcurrent protection to protect the conductors

#### EV.7.6.5
Battery packs with Low Voltage or non voltage rated fusible links for cell connections may be used when all three conditions are met:
- An Overcurrent Protection device rated at less than or equal to one third the sum of the parallel fusible links and complying with EV.7.6.2.b above is connected in series.
- The AMS can detect an open fusible link and will Open the Shutdown Circuit EV.8.2.2 if a fault is detected.
- Fusible link current rating is specified in manufacturer’s data or suitable test data is provided.

#### EV.7.6.6
Cells with internal Overcurrent Protection may be used without external Overcurrent Protection if suitably rated
Most cells internal protection will fall under [[#EV.7.6.5]]