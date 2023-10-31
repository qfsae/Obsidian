# VCU WiFi Expansion Card
## Purpose
The WiFi expansion card serves two main purposes. First, it serves its primary purpose of expanding the VCU to include WiFi capabilities. Secondly, it will serve as a learning experience for developing stacked PCBs and the combining of two microcontrollers.

The idea behind the project is to be able to connect the VCU into a WiFi network, and thus into some ones laptop. Ideally, we will create our own monitoring software that will interface with the VCU similar to MoTec's M1 Tune, and how we tuned the engine at testing in Q23.

The first step in accomplishing this goal is to create the hardware behind the VCU-WiFi interface. When the VCU was under development, the original idea was to do this over Serial communication between an ESP8266 (WiFi enabled microcontroller) and the STM32 that runs the VCU. This may be adapted as needed. Refer to [[VCU Exposed Hardware]].

## Rules
The current design does not anticipate this component being used outside of testing. Therefore, it is not mandatory to follow any rules. However, some rules should be taken into consideration:
- [[EV.7.7 Grounding]]
- [[EV.5.4 Grounded Low Voltage System]]

## Design Notes
This project integrates with two others:
- [[Remote Monitoring Dashboard]]
- [[Remote Monitoring Firmware]]