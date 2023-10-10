This check must be implemented in addition to the [[EV.8.7 BSPD]] and is intended to catch BSPD faults before they trip the BSPD relay.
#### EV.5.7.1 Shutdown Conditions
The power to the motors must be immediately and completely shut down when two of the following exist at the same time:
- The mechanical brakes are engaged [[T.4 ETC Components]]
- The APPS signals more than 25% pedal travel [[T.4 ETC Components]]
This must be demonstrated at Technical Inspection
#### EV.5.7.2 Reset
The Motor shutdown must remain active until the APPS signals less than 5 percent travel, with or without brake operation