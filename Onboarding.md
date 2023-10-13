# Onboarding
All incoming team members will be required to complete an onboarding project. Start by completing the [[#GitHub Onboarding]]. This is mandatory for all members. Once complete, you can do either the software, electrical, or both onboarding projects. Please complete the project that reflects what parts of the car you wish to work on.

## GitHub Onboarding
The Electrical Team uses GitHub to store and organize all of our files, including this notebook! If you are reading this on GitHub, congratulations, you are already 1/4 done. Only three steps left!
#### 1. Download Obsidian/GitHub Desktop
Obsidian can be downloaded from: https://obsidian.md/download
GitHub Desktop can be downloaded from : https://desktop.github.com/
If you want to use Git Bash, that will be fine, however desktop is suggested because of its ease of use.

#### 2. Setting up GitHub Desktop
In order to contribute to projects, you need to clone our FSAE repositories. Start by opening file explorer and navigating to where you would like to store the repositories. The `Documents` folder is recommended. Create a new folder called `QFSAE`, or whatever you would like to call it. Do not leave spaces in the name. Open GitHub Desktop. Select `File` -> `Clone Repository`, then find the `qfsae/Obsidian` repository and select it. Choose the folder you set up earlier, and select `Clone`. Repeat the same steps for `qfsae/zenith` and `qfsae/pcb`. You now have access to all of the QFSAE files!

#### 3. Setting up Obsidian
Open Obsidian and select `open folder as vault`. Navigate to the folder you made within [[#2. Setting up GitHub Desktop]]. Once here, select the `Obsidian` folder and select `Select Folder`. Once open, you can see this design notebook! If prompted, select `enable plugins` or `I trust this repository`.
By default, Obsidian comes with VIM keybinds turned on. If you don't know what these are, or don't want to use them, click the settings icon on the bottom left of Obsidian, make sure you are under the `Editor` page of the settings, then scroll to the bottom and turn off `Vim key bindings`.

Congratulations! You have now completed all of the required software set up!
If you want to know a little more about Obsidian, it is recommended to read the [[ReadME]]. Please reference it when making PRs into this notebook.

The next step is to setup either Altium (if you want to work on PCBs), or VS Code (if you want to work on firmware).
If you are in Powertrain and reading this, you can safely return to SolidWorks.

## Software Onboarding
Software Onboarding will consist of developing firmware for a "CAN probe" that runs on an STM32 or an Arduino. For those less experienced, it is recommended to start with the Arduino. For those more experienced, you may choose to write the code using the Arduino HAL on the STM32, or simply write it bare metal style.

#### Installing Software
To get started on this project you will need to install VS code. Once installed, you will also need to add the `PlatformIO` plugins.

#### Getting Started
###### 1. Creating a Branch
The first step in creating a new project is to create a new branch on the GitHub repository. Since this is a code project, we will be working in the `qfsae/zenith` repo. Start by opening GitHub desktop and selecting the Zenith repository. You can do this by clicking `current repository` in the top left and then by selecting `zenith` under `qfsae`.  Finally click the `current branch` button to the right of the right of the `current repository` button. At top left click `New branch` and name the branch `firstname_lastinitial_canprobe_q24`, changing out `firstname` and `lastinitial` with your own first name and the first letter of your last name. You are now ready to open VS code and create your project.
###### 2. Creating a PlatformIO Project
Now that you have created a branch on the Zenith repository, you need to create you project code. Start by opening VS Code and selecting the alien on the left hand side of the screen. Click `Create New Project`. Name the project `canprobe` and change the location to be in the root directory of the Zenith repository. Then, select the board and framework you would like to use. For beginners, select Arduino Uno. You can type to search. For more experienced users, you might chose to use STM32. In that case, select `STM32F446RE` as the board.
Finally choose the framework. For this project, using the Arduino Framework is recommended, however if you are interested you could also do it with CMSIS. This is using the vendor files to create a bare metal program.
Note that you are not working from scratch here, so it is not true "bare metal", but it is very close. The only difference is that they linker and bootloader are set up for you with PlatformIO CMSIS.
Once you have chosen the Framework, click finish. PlatformIO will create the project for you. If you chose bare metal, then you can skip this next step.
If you are working with Arduino, you will need to include the `seeed-studio/CAN_BUS_Shield` library. If you are working with STM32 Arduino HAL, you will need to include the `jchisholm204/st-f4can` library. You will also need to include the build flag `-DENABLE_HWSERIAL2` and ensure that the `upload_protocol` is correctly configured. You are now ready to start writing your code.

#### Project Requirements
Your code should be able to run on your platform of choice:
- Arduino + CAN Bus Shield
- STM32 + Arduino HAL
- STM32 Bare Metal
For this project, we will assume that the [[VCU]] sends out a CAN message with the following format:
- ID: `0x280`
- Len: `6`
- Byte 0: Motor RPM (1/100 multiplier) (RPM)
- Byte 1: Drive Status (Boolean Values)
	- Bit 0: TS Active
	- Bit 1: BMS Fault
	- Bit 2: Temp Fault
	- Bit 3: Inverter Fault
	- Bit 4: VCU Fault
	- Bit 5: Throttle Fault
	- Bit 6: Brake Fault
- Byte 2: Vbatt Voltage (0.1421 multiplier) (V)
- Byte 3: Motor Power (16 bit) (W)
- Byte 4: Motor  Power2 (16 bit) (W)
- Byte 5: Coolant Temperature (C)

You will write a program for your target architecture that will receive this information over CAN and print it out to a serial terminal. There will be other messages on the CAN bus besides this one. Hint: You will need to filter by CAN ID.

You may want to do some research on CAN Bus before you attempt this project. <a href="https://github.com/qfsae/zenith/blob/master/docs/can.pdf">Here</a> is a great resource written by one of our past captains, Ethan Peterson, to get you started.
#### References
- <a href="https://github.com/qfsae/zenith/blob/master/docs/can.pdf">CAN Bus White Paper</a>
- [[CAN bus general info]]
- <a href=https://github.com/qfsae/zenith/tree/master/dyno-can/arduino-can-monitor>Example Code</a>
	- For Arduino only
	- Does not complete project requirements
- Leads run tutorial sessions -> Check Teams!

#### Completion
While I will advise that you backup your code to your GitHub branch frequently, the only requirement is that you push your final code to GitHub as instructed in the [[#Software Onboarding#Getting Started]] section.


## Electrical Onboarding
Electrical onboarding will consist of designing a brake light for the car.
Project requirements are listed in: [[Brake Light]].

#### Installing Software
To get started on this project, you will need to install Altium. Altium is the PCB design software used by the team. You can obtain an Altium license for free as a student. The team also has a limited number of Altium licenses available. Since there is already a comprehensive guide available on our <a href="https://github.com/qfsae/pcb">PCB Repository</a> it will not be included here.

#### Getting Started
The first step in creating a new project is to create a new branch on the GitHub repository. Since this is a PCB project, we will be working in the `qfsae/pcb` repo. Start by opening GitHub desktop and selecting the PCB repository. You can do this by clicking `current repository` in the top left and then by selecting `pcb` under `qfsae`.  Finally click the `current branch` button to the right of the right of the `current repository` button. At top left click `New branch` and name the branch `firstname_lastinitial_brakelight_q24`, changing out `firstname` and `lastinitial` with your own first name and the first letter of your last name. You are now ready to open Altium and create your project.

#### References
- <a href="https://www.youtube.com/watch?v=PqFtSpAXB9Q">Altium Tutorial</a>
- Leads run tutorial sessions -> Check Teams!

#### Completion
While I will advise that you backup your code to your GitHub branch frequently, the only requirement is that you push your final code to GitHub as instructed in the [[#Electrical Onboarding#Getting Started]] section.

It is recommended that you attempt the project on your own, but the team does not expect new members to be familiar with Altium so we will be running tutorials in the first few weeks. Keep a close eye on the Electrical Teams chat for when they are happening.