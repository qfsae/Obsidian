See: https://www.eurocircuits.com/blog/formula-electric-belgium-own-electronic-control-unit-with-eurocircuits-pcbs-3/ for an example

# Voltage Indicator PCB Project
## Purpose
The main purpose of the voltage indicator PCB is to alert the team when [[T.9 Electrical Equipment#T.9.1 Definitions|High Voltage]] is present at the Accumulator terminals. It will do this through a labeled LED placed on the outside of the Accumulator Container. The design must be fully analog, and adhere to galvanic isolation between the GLV and HV Systems. It is recommended to power the LED through the TS Accumulator power. It is also recommended to assume the LED placed on the outside of the Accumulator container will not be soldered to the board, but will instead be connected through wires and a header.

## Rules
As always, the rules listed below are for reference only. They may be incomplete. It is the shared responsibility between the entire team to ensure that all FSAE design rules are being met. If this list is missing something, please submit a PR (Pull Request).
- [[EV.6.7 Voltage Indicator]]
- [[EV.7.2 Insulation]]
- [[EV.7.5 Voltage Separation]]
- [[EV.7.6 Overcurrent Protection]]
- [[EV.7.7 Grounding]]

## References
Here are some references to get you started. It is expected that you do your own research for this project. If you feel like it, you could also open a PR and add your sources here.
- https://www.reddit.com/r/FSAE/comments/x6fjfa/voltage_indicator/
- Example -> https://www.eurocircuits.com/blog/formula-electric-belgium-own-electronic-control-unit-with-eurocircuits-pcbs-3/ 
- https://www.cameronord.one/projects/fsae_voltage_indicator
- https://www.wisconsinracing.org/wp-content/uploads/2020/10/WR-217e_Accumulator_Design.pdf