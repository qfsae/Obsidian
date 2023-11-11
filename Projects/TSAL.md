# Tractive System Active Light (TSAL)
## Purpose
The purpose of the TSAL is to alert surrounding persons that the car's tractive system is active. More specifically, that there is high voltage present at the Accumulator terminals.

The TSAL will consist of two components. First is the control PCB. This PCB will be connected to the HV and GLV systems. It will control the second component of the TSAL which is the TSAL light itself. The TSAL will be mounted in the roll hoop according to FSAE regulations. The LED could be an internal PCB project or a purchased component.

## Rules
As always, the rules listed below are for reference only. They may be incomplete. It is the shared responsibility between the entire team to ensure that all FSAE design rules are being met. If this list is missing something, please submit a PR (Pull Request).
- [[EV.6.9 TSAL]]
- [[EV.7.2 Insulation]]
- [[EV.7.5 Voltage Separation]]
- [[EV.7.6 Overcurrent Protection]]
- [[EV.7.7 Grounding]]
- [[EV.8.8 Interlocks]]

## References
Design Walkthrough:
https://michaelruppe.com/2020/10/11/design-walkthrough-tractive-system-active-light-tsal-driver-fsae/

Example KiCad PCB
https://github.com/michaelruppe/FSAE/tree/master/TSALv3

Design

Isolated Power Supply & TSAL Light Interconnect
Need a 2W DC-DC Converter, 12V output voltage, 9-18 V input voltage, single output


Optocoupler, Phototransistor Output, with Base Connection
https://www.vishay.com/docs/81181/4n35.pdf
https://www.snapeda.com/parts/4N35/Vishay%20Semiconductor%20Opto%20Division/view-part/

obsidian://open?vault=Obsidian&file=assets%2FData%20Sheet%20500V.pdf



Differential Comparator, get through hole for easy soldering
https://www.ti.com/lit/ds/symlink/lm211.pdf?HQS=dis-dk-null-digikeymode-dsf-pf-null-wwe&ts=1698680288064&ref_url=https%253A%252F%252Fwww.ti.com%252Fgeneral%252Fdocs%252Fsuppproductinfo.tsp%253FdistId%253D10%2526gotoUrl%253Dhttps%253A%252F%252Fwww.ti.com%252Flit%252Fgpn%252Flm211

NE555 (Precision Timer), this is used for precision timing circuits capable of producing accurate time delays or oscillation.
https://www.digikey.ca/en/products/detail/texas-instruments/NE555P/277057
https://www.snapeda.com/parts/NE555P/Texas%20Instruments/view-part/


high voltage resistor 