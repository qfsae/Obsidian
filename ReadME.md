# ReadME

Obsidian Repository for QFSAE Q24-25 EV conversion. Contains daily notes, design review notes, project writeups, rules and more. Everything associated to QFSAE during the EV transition should be documented in this log for future reference. Ideally, this will simplify debugging once the current team has graduated.

## Organization
Folders are used as the primary organizational method. Obsidian document tags can also be used for organizing the graph view.

### Folders
- All rules contained in the `/Rules` folder.
	- These are the FSAE rules from 2023 (some have been updated to 2024)
	- All rules content is searchable by the Obsidian search bar
- All team projects are contained within the `/Projects` folder
	- Projects are separated by where they are in regards to the rules
	- The [[Projects Master List]] document can be used to track project progress
	- `/High Voltage` Contains all projects relating to the Tractive System
	- `/Low Voltage` Contains all of the projects relating to the GLV System
	- `/Shutdown` Contains information on the shutdown circuit
	- `/VCU` Contains some preliminary information about the Vehicle Control Unit
- Daily notes and design review notes are within the `/Daily Notes` folder. These contain notes from  various team meetings and design reviews. *This folder is mostly for use by the team lead/s*
- `/Documentation` Is for team written documentation
	- Custom PCB's, API's, ...
- `/Datasheets` Is used to store datasheets for purchased components
- `/CAN Bus` Contains all information about the CAN Bus
	- Protocols used by purchased devices
	- Protocols implemented by the team on custom boards
	- Master list of all bus messages
- `/Team Info`
	- Onboarding Documentation
	- List of borrowed parts
- `/Components Info` Summarized notes on purchased components
- `Components Research` Research on purchasing components
### Project Tags
- Not Started = `notag` (Pink)
- In Progress = `#PROJECT_IP` (Blue)
- Ready for/in Design Review = `#PROJECT_DR` (Yellow)
- Complete  = `#PROJECT_C` (green)

## Using Obsidian
This notebook, while consisting of Markdown files, is designed to be used within Obsidian. Using Obsidian allows the pages to link properly and also supports searching of the entire notebook.

Obsidian can be downloaded from https://obsidian.md/download. 
#### Getting Started
To get started working on this notebook, talk to one of the Electrical/Firmware/Power Electronics leads about getting access to the FSAE GitHub Organization. Once you are added, you will have write access to our repositories, including this notebook.

#### Contributing
This main branch notebook is write protected, in order to contribute to it, you have to create a new branch and edit it there.
Once you are finished, open a Pull Request (PR) to merge your changes to the main branch of the notebook.
When submitting a PR, add your project manager and team lead to the PR. Once they read over your changes, they will OK the merge.
When submitting a PR, remember to not include your `.obsidian` configuration.
#### Tips
Some helpful tips for navigating this notebook:
- Hold control and hover over linked notes to be able to quickly read them (This only works inside of Obsidian, NOT on Git)
- Do not use the "Daily Notes" feature - This is for major design notes only, meant to be used by the team leads.
- Use the graph to quickly see what other projects connect to yours