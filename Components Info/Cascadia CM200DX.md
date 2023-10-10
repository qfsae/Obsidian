## Specifications
- 50-480VDC operating voltage
- 300Arms Continuous Current
- 740Arms Peak Current (30 seconds, cooling dependent)
- 225kW Peak output power
- 650μF DC Bus Capacitance
- 6.75 kg
- <1 second discharge to motor
- <120 second passive discharge
- 9-32VDC GLVS (Grounded Low Voltage System)
- 12 kHz PWM Switching Frequency
- Variable PWM rate (6-12 kHz)

### Inverter IO
- 4 Analog Inputs (5V Tolerant)
- 2 RTD Inputs
	- RTD (Resistance Temperature Detector)
	- Supports PT100 and PT1000
- 2 High Side Driver Outputs
- 2 Low Side Driver Outputs
- Single Resolver input
- 1 Sin-Cos Encoder Interface (only present on -SP option)
- 2 [[CAN bus]] Channels
	- 125-1000kbps
	- adjustable offset
	- J1939 compatible
	- .dbc messaging
	- uses grounded sheilding
- RS232 for programming and diagnostics

### Power Scheme (GLVS)
- 12/24V Constant Power
	- required at all times
	- Inverter remains in "sleep" mode while active
- Switched 12/24V
	- Powers up inverter
	- signals to start CAN communications
- Safety Switched 12/24V
	- Required to run motor
	- If removed, Inverter will declare hardware gate fault and shut down TS (Tractive System)
- Common Ground used for all power schemes

## Supplemental Parts

### GLV Connector #CRIMPS 
<a href="https://www.youtube.com/watch?v=7ZNe4qvVlCk">How to Assemble YouTube</a>
- Mating Housing - Molex CMC 48
	- <a href="https://www.molex.com/en-us/products/part-detail/643203311">Molex</a> ~ $14.15 USD
	- <a href="https://canada.newark.com/molex/64320-3311/automotive-conn-housing-rcpt-48ways/dp/84R1292">Newark Canada</a> ~ $26.53
	- <a href="https://www.mouser.ca/ProductDetail/Molex/64320-3311?qs=WeK9NnMzqvcb7xofj9yxAA%3D%3D">Mouser</a> ~ $20.52
	- <a href="https://www.digikey.ca/en/products/detail/molex/0643203311/2424531">DigiKey</a> ~ $24.83
- Strain Relief - Molex 64320-1301
	- <a href="https://www.mouser.ca/ProductDetail/Molex/64320-1301?qs=WeK9NnMzqvdDwPMfqfvNDA%3D%3D">Mouser</a> ~ $1.31
	- <a href="https://www.digikey.ca/en/products/detail/molex/0643201301/2424529">DigiKey</a> ~ $1.44
	- <a href="https://canada.newark.com/molex/64320-1301/dust-cap-cover-wire-cap-cmc-64320/dp/66W2186">Newark</a> ~ $ 1.52
- Molex 64322-1239
	- 20AWG
	- Wire OD 1.4-1.7 mm
	- CP 0.6
	- <a href="https://www.molex.com/en-us/products/part-detail/643221239">Molex</a> ~ $0.56
	- <a href="https://www.mouser.ca/ProductDetail/Molex/64322-1239?qs=WeK9NnMzqvcxOB%2FeCJyBww%3D%3D">Mouser</a> ~ $0.81
	- <a href="https://www.digikey.ca/en/products/detail/molex/0643221239/2523193">DigiKey</a> ~ $0.82
- Molex 64322-1219
	- 18AWG
	- Wire OD 1.4-1.7 mm
	- CP 0.6
	- <a href="https://www.mouser.ca/ProductDetail/Molex/64322-1219?qs=WeK9NnMzqveJTQH%2Ful1xdw%3D%3D">Mouser</a> ~ $0.80
	- <a href="https://www.digikey.ca/en/products/detail/molex/0643221219/3044372">DigiKey</a> ~ $0.82
- Molex 64323-1319
	- 18AWG
	- Wire OD 1.4-2.15 mm
	- CP 1.5
	- <a href="https://www.mouser.ca/ProductDetail/Molex/64323-1319-Loose-Piece?qs=%2FH84ApbqrvN52jJqwAe7%252BA%3D%3D">Mouser</a> ~ $1.28
	- <a href="https://www.digikey.ca/en/products/detail/molex/0643231319/2523198">DigiKey</a> ~ $1.22
- CP 0.6 Bind Plug - Molex 643251010
	- <a href="https://www.molex.com/en-us/products/part-detail/643251010">Molex</a> ~ $0.16
	- <a href="https://www.mouser.ca/ProductDetail/Molex/64325-1010?qs=WeK9NnMzqvdqzL38QpeKFQ%3D%3D">Mouser</a> ~ $0.23
	- <a href="https://www.digikey.ca/en/products/detail/molex/0643251010/2523211">DigiKey</a> ~ $0.25
- CP 1.5 Bind Plug - Molex 643251023
	- <a href="https://www.mouser.ca/ProductDetail/Molex/64325-1023?qs=WeK9NnMzqvdN0YdcngDMkw%3D%3D">Mouser</a> ~ $0.22
	- <a href="https://canada.newark.com/molex/64325-1023/wire-plug-cmc-connector/dp/84R1295">Newark</a> ~ $0.25
	- <a href="https://www.digikey.ca/en/products/detail/molex/0643251023/2523212">DigiKey</a> ~ $0.26

### Inverter High Voltage #CRIMPS 
CM200 Product models use Rosenberger HPK family connectors for all high voltage connections.
See product page <a href="https://www.rosenberger.com/product/hpk/">here</a>. 
Recommended to order from Cascadia with Inverters. Ask for model number during order process for future reference.

### Pre Charge Circuitry 
- External Pre-Charge must be used to protect internal inverter capacitors.
- Cascadia can provide the following pre charge components for DX inverters
	- Relay -> 30A Cont. Current, 12V activation voltage, p/n = 77-0026
	- Resistor -> 600 Ohm, 50W, p/n = 53-0006
	- Fuse -> 5A, 500V, p/n = G1-0013-01
- Recommended parts: Page 32 of [[PM CM and RM Hardware User's Manual (V3_7) (1).pdf|Hardware User Manual]] 

### Required Components
- RS232 Adapter for programming
- HVTS/GLV Crimps/Connectors

### Datasheets
- [[PM CM and RM Hardware User's Manual (V3_7) (1).pdf]]
- [[Inverter Discharge Process (V0_9).pdf]]
- [[Setting up the Emrax Motor V1_2 (1).pdf]]