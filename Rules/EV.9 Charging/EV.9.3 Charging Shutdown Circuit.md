## EV.9.3 Charging Shutdown Circuit
#### EV.9.3.1
The Charger Shutdown Circuit consists of:
- The [[EV.9.2 Charger Features#EV.9.2.7 Shutdown Button]]
- [[EV.8.3 AMS]]
- [[EV.8.6 IMD]]

#### EV.9.3.2
The AMS and IMD parts of the Charger Shutdown Circuit must:
- Be designed as Normally Open contacts
- Have completely independent circuits to open the Charging Shutdown Circuit
- Design of the circuits must ensure that a failure cannot result in electrical power being fed back into the Charging Shutdown Circuit

## EV.9.4 Charging Shutdown Circuit Operation

#### EV.9.4.1
When charging, the [[EV.8.3 AMS]] and [[EV.8.6 IMD]] must:
- Monitor the Accumulator
- Open the Charging Shutdown Circuit if a fault is detected

#### EV.9.4.2
When the Charging Shutdown Circuit opens:
- All current flow to the Accumulator must stop immediately
- The Voltage in the TS must be [[T.9 Electrical Equipment#T.9.1 Definitions|Low Voltage]] in 5 seconds or less
- The charger must be turned off
- The charger must remain disabled until manually reset