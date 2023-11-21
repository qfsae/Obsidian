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