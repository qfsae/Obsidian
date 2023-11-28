**Background Research:**
EVSE:
- Electric Vehicle Supply Equipment is the technical name for charging stations for electric vehicles.
- They provide electric power to the vehicle, as such recharging the accumulator.
- EVSE systems include typical electric components to conduct energy transfer
- EVSEs do not handle charging the accumulator, which is internal to the car itself, but directs energy to the charging port

Levels:
* Level 1 AC chargers intake from a 120V typical home wall outlet, and delivers power to the accumulator accordingly
	* Incredibly slow, at 12-16A, and charge 1.4-1.9kW, charging minimal kilometres of range per hour
* Level 2 AC chargers intake 240V (sometimes 208V), and supply power to the accumulator. Permanently wired to a dedicated circuit of the supplied voltage within a garage and/or driveway for typical EV vehicles.
	* Between 12 and 80 amps of charge is typically supplied
		* Most commonly 30-32A
	* Adding the two together, power ranges from 2.88kW to 19.2kW (usually top out at 12kW though)
		* With 30-32A, 7.2kW-7.68kW
	* Cost approximates from $500-$2000 USD for consumer products.
	* Compatible with industry-standard SAE J1772 (commonly refered to as "J-plug")
* Level 3 DC fast charging stations intake from either a 240V (sometimes 208V) or 480V outlet on the grid it is hardwired to, and delivers power to the accumulator. Can also be 1000V, but those are not found at an EV homeowner's residence.
	* Amperage is below 125A, typically 60A
	* Charging loads usually start at 50kW and go up to 400kW and 900kW (depends on voltage standard and amperage supply)
	* Compatible usually fall under one of the three standards: Superchargers (Tesla), SAE CCS (European EVs), and CHAdeMO (Asian EVs)

**Formula E:**
Regulation cuts:
* [[EV.9.2 Charger Features]] lists under EV.9.2.1 that the charger must be a galvanically isolated AC input to DC output, immediately cutting off potential use of Level 3 charging stations, which uses DC input
	* The incredibly slow speed of Level 1 chargers further implies that the right charging solution is a Level 2 charger implementation

**Other teams:**
* Research looking at past solutions developed by FSAE teams included a commonly presented power supply, specifically Elcon chargers, and more specifically the HK-J UHF models

**Chargers:**
Elcon HK-J 6.6kW charger:
* Uses CANbus (can be bought with/without one)
* Designed for electric vehicle LiFePO4/lithium/Lead acid battery and battery management system interface
* Specs mention up to 95% power efficiency and over 93% full load efficiency
* Input voltage range from AC90V to AC265V (45Hz-65Hz)
* Output DC range depends on model:
	* HK-J-H66-80: 18-68VDC Max DC output voltage range, 80A Max Current
	* HK-J-H99-80: 25-99VDC Max DC output voltage range, 80A Max Current
	* HK-J-H132-64: 34-132VDC Max DC output voltage range, 64A Max Current
	* HK-J-H198-46: 50-198VDC Max DC output voltage range, 46A Max Current
	* HK-J-H440-20: 110-440VDC Max DC output voltage range, 20A Max Current
	* HK-J-H650-12: 170-650VDC Max DC output voltage range, 12A Max Current
* Cost ranges across websites, no clear price range, but typically does not exceed 2000 USD

**Plan of Action:**
With research on other chargers in mind, the Elcon HK-J 6.6kW seems to be the most viable solution, as others usually limit at 450VDC, meanwhile the accumulator sits at 464VDC. Specifically the HK-J-H650-12 supports the input AC voltage/current supplied by FSAE during competition, and matches the voltage standard our battery limits, that being 464VDC. As such, assuming an order can be made of this charger, all that's remaining is dealing with the charging shutdown circuit, as well as the charging port.

**Charging Port:**
As the level of charging can presumably be concluded to be targeted for level 2 charging (as such is provided by FSAE during competition, and 120V charging is incredibly slow in comparison), the plug required must be the J1772, as stated by the provided charging from FSAE during competition: https://www.fsaeonline.com/cdsweb/gen/DownloadDocument.aspx?DocumentID=07af1b6a-f8ff-45b1-ba5e-1ced61d70d5c
Therefore, a J1772 plug supporting the voltage/current thresholds of 20A and 208V from an AC supply must be accomodated.
The following are two products found from electricmotorsport.com, which may not be an ideal order location, but does show some options for the charger:
* J1772 32A Plug and UL Cable 5m with Dust Cover: https://www.electricmotorsport.com/ev-parts/chargers/j1772/j1772-32a-plug-cord.html
	* This charger provides the UL cable connected to the charging port itself
* J1772 32A Receptacle V3 w/ Terminals & Hardware: https://www.electricmotorsport.com/ev-parts/chargers/j1772/j1772-32a-receptacle-ver-2.html
	* This charger does not provide the UL cable, and therefore must be developed following purchase
There also exists the Active Vehicle Side Control Board Module, which may be of aid for achieving safety standards declared by FSAE, and/or provide guidance to covering said rules: https://www.electricmotorsport.com/ev-parts/chargers/j1772/avc2-module.html

**Charging Shutdown Circuit:**
[[EV.9.3 Charging Shutdown Circuit]] states the purpose of the development of the charging shutdown circuit. The goal is to use readings from the [[EV.8.3 AMS]] and [[EV.8.6 IMD]] to determine if the charging shutdown circuit must be triggered, which would be when readings are at critical points. In real-world application to EV conversions, it is common to see this being done with the CAN Bus Shunt, which measures readings of current, voltage, and temperature, for BMS systems. See the following of an example item from DigiKey: https://www.digikey.com/en/product-highlight/i/isabellenhuette/ivt-s-current-voltage-and-temperature-sensors
The CAN Bus Shunt may be of good reference to how it may be possible to develop an appropriate for measuring voltage, current, and temperature, while the charging shutdown circuit can be developed around these readings. The Elcon HK-J-H650-12 can be bought with a CAN bus to retrieve information, which may also be integral to the development of the shutdown circuit.
What comes next with the circuit is the development of the model (to be done presumably in Altium), but before this comes discussion and approval from the electrical leads on deciding which options to pursue.