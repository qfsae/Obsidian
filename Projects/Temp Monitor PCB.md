# Temperature Monitor Board
## Purpose
According to FSAE rules, battery cell voltages and temperatures must be monitored by the AMS. The [[Orion 2 BMS]] will monitor the cell voltages and up to 8 temperature inputs. However, this is insufficient for FSAE rules. Therefore, in order to monitor ALL of the battery cell temperatures, the team will be designing a Temperature Monitor PCB. This PCB will be part of the HV and GLV system. It will serve as the second part of the [[EV.8.3 AMS]] in addition to the [[Orion 2 BMS]]. As such, it will be responsible for monitoring the Accumulator conditions and opening the shutdown circuit in case of a fault.

## Rules
As always, the rules listed below are for reference only. They may be incomplete. It is the shared responsibility between the entire team to ensure that all FSAE design rules are being met. If this list is missing something, please submit a PR (Pull Request).
- [[EV.8.3 AMS]]
- [[EV.7.2 Insulation]]
- [[EV.7.5 Voltage Separation]]
- [[EV.7.6 Overcurrent Protection]]
- [[EV.7.7 Grounding]]
- [[EV.8.5 Accumulator Temperature]]
- [[EV.8.1 Shutdown Circuit]]
- [[EV.6.2 Electrical Configuration]]

## Design Notes
[[EV.8.5 Accumulator Temperature#EV.8.5.7 Isolation]] can be met by using isolated ADC's for temperature sensor measurement.

### Relevant Documents
- [[Orion 2 BMS]]
- [[Sony VTC6]]
- [[VTC6-Sony-Murata-Li-ion-Battery-Module-With-Temperature-Sensor-Datasheet-Tesla-Battery-Sponsorship-Formula-SAE-Electric-Formula-Student-Battery-Pack.pdf]]