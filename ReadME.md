# ReadME

Obsidian Repository for QFSAE Q24 EV conversion. Contains daily notes, design review notes, project writeups, rules and more. Everything associated to QFSAE during the EV transition should be documented in this log for future reference. Ideally, this will simplify debugging once the current team has graduated.

## Organization

### Project Tags
- Not Started = `notag` (Pink)
- In Progress = `#PROJECT_IP` (Blue)
- Ready for/in Design Review = `#PROJECT_DR` (Yellow)
- Complete  = `#PROJECT_C` (green)

### Folders
- All rules contained in the `/Rules` folder. These are the FSAE rules from 2023 (latest available)
- All projects are contained within the `/Projects` folder
- Daily notes and design review notes are within the `/Daily Notes` folder. These contain notes from  various team meetings and design reviews. Notes in this folder should not be modified without explicit permission

### CAN Bus
- Everything related to the Q24 CAN Bus should be stored in this folder
- Check the list before assigning a new CANID
- Add ALL CANID's to the list once added
- Proper documentation is key to not having message conflicts
- Cassedia/Orion's CAN protocols will need to be added before anything custom

## Using Obsidian
Obsidian can be downloaded from https://obsidian.md/download. 
#### Getting Started
To get started working on this notebook, talk to one of the Electrical/Firmware/Power Electronics leads about getting access to the FSAE GitHub Organization. Once you are able to view the view our repositories, you will have access to this notebook.
#### Contributing
This notebook is write protected, in order to contribute to it, you have to create a new branch and edit it there. Once you are finished, open a Pull Request (PR) to merge your changes to the main notebook. Add your project manager and team lead to the PR, and one they read over your changes, they will OK the merge. When merging, remember to not merge your `.obsidian` configuration.
#### Tips
Some helpful tips for navigating this notebook:
- Hold control and hover over linked notes to be able to quickly read them (This only works inside of Obsidian, NOT on Git)
- Do not use the "Daily Notes" feature - This is for major design notes only, meant to be used by the team leads.
- Use the graph to quickly see what other projects connect to yours