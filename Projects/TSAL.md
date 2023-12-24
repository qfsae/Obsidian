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



## LV Components
(Based off of the TSALv3 by Michael Ruppe)

Chips & Mosfets: 
- [MCT06P10-TP Mosfet](https://www.digikey.ca/en/products/detail/micro-commercial-co/MCT06P10-TP/10054657) (Need 2)
- [4N35 Octocoupler ](https://www.digikey.ca/en/products/detail/lite-on-inc./4N35/385766?utm_adgroup=&utm_source=google&utm_medium=cpc&utm_campaign=PMax%20Product_Low%20ROAS%20Categories&utm_term=&productid=385766&utm_content=&utm_id=go_cmp-20291741422_adg-_ad-__dev-c_ext-_prd-385766_sig-CjwKCAiAp5qsBhAPEiwAP0qeJoo0xd6mFl1-JjWuJWyxxQXLfvYd5w1Y0USnafQJdsmYGCilU4m-qBoCE8kQAvD_BwE&gad_source=1&gclid=CjwKCAiAp5qsBhAPEiwAP0qeJoo0xd6mFl1-JjWuJWyxxQXLfvYd5w1Y0USnafQJdsmYGCilU4m-qBoCE8kQAvD_BwE) 
- [NE555 Timer](https://www.digikey.ca/en/products/detail/texas-instruments/NE555P/277057?utm_adgroup=&utm_source=google&utm_medium=cpc&utm_campaign=PMax%20Product_Medium%20ROAS%20Categories&utm_term=&productid=277057&utm_content=&utm_id=go_cmp-20291741266_adg-_ad-__dev-c_ext-_prd-277057_sig-CjwKCAiAp5qsBhAPEiwAP0qeJhWZgpNMj2Bg6ZjUakRIIaQB_IBYAS7WLkcLrBT3-1zAB45qPkCG1BoCpBoQAvD_BwE&gad_source=1&gclid=CjwKCAiAp5qsBhAPEiwAP0qeJhWZgpNMj2Bg6ZjUakRIIaQB_IBYAS7WLkcLrBT3-1zAB45qPkCG1BoCpBoQAvD_BwE)
- [2N7002 Mosfet](https://www.digikey.ca/en/products/detail/onsemi/2N7000/244278?utm_adgroup=&utm_source=google&utm_medium=cpc&utm_campaign=PMax%20Supplier_Focus%20Supplier&utm_term=&productid=244278&utm_content=&utm_id=go_cmp-20282403582_adg-_ad-__dev-c_ext-_prd-244278_sig-CjwKCAiAp5qsBhAPEiwAP0qeJpG17yl39JdT1NKztfdFC_N3SQm6Rf_zKSay0UzbEiYHL8QHUPQHLRoCLL0QAvD_BwE&gad_source=1&gclid=CjwKCAiAp5qsBhAPEiwAP0qeJpG17yl39JdT1NKztfdFC_N3SQm6Rf_zKSay0UzbEiYHL8QHUPQHLRoCLL0QAvD_BwE) (Need 2)

Other Components:

- Red LED (12v)
	- [Possible Red LED](https://www.digikey.ca/en/products/detail/w%C3%BCrth-elektronik/150060RS75000/4489901) (Not necessary, just for debugging) The actual LEDs get powered by GRN+ and RED+ outputted using the J1 connector. 
- Miscellaneous Capacitors and Resistors
	- Capacitors:
		- [1 µf cap](https://www.digikey.ca/en/products/detail/kemet/C0805C105M3REC7210/19187599?utm_adgroup=Kemet&utm_source=google&utm_medium=cpc&utm_campaign=PMax%20Shopping_Supplier_Kemet&utm_term=&productid=19187599&utm_content=Kemet&utm_id=go_cmp-17861998787_adg-_ad-__dev-c_ext-_prd-19187599_sig-CjwKCAiAp5qsBhAPEiwAP0qeJiifoK9KTxF9DXGEaa5OqBMW5vinpKY3If_sfeC92sSJIbInDmQ2IhoCUGYQAvD_BwE&gad_source=1&gclid=CjwKCAiAp5qsBhAPEiwAP0qeJiifoK9KTxF9DXGEaa5OqBMW5vinpKY3If_sfeC92sSJIbInDmQ2IhoCUGYQAvD_BwE)
		- [100 nf cap](https://www.digikey.ca/en/products/detail/kemet/C0805C104K1RAC7210/12701997?utm_adgroup=Kemet&utm_source=google&utm_medium=cpc&utm_campaign=PMax%20Shopping_Supplier_Kemet&utm_term=&productid=12701997&utm_content=Kemet&utm_id=go_cmp-17861998787_adg-_ad-__dev-c_ext-_prd-12701997_sig-CjwKCAiAyp-sBhBSEiwAWWzTntraiBomYjlGryWnJJFNXKRcj3UbT1ZEJXd9ZInZiOzLvQmsZT3lVRoCVUwQAvD_BwE&gad_source=1&gclid=CjwKCAiAyp-sBhBSEiwAWWzTntraiBomYjlGryWnJJFNXKRcj3UbT1ZEJXd9ZInZiOzLvQmsZT3lVRoCVUwQAvD_BwE) (Need 2)
	- Resistors: (Before Finding links go over what is needed)
		- [10kΩ](https://www.digikey.ca/en/products/detail/yageo/CFR-12JR-52-10K/17679) (Need 2)
		- [22kΩ](https://www.digikey.ca/en/products/detail/yageo/CFR-25JR-52-22K/12006) (Need 2)
		- [500Ω](https://www.digikey.ca/en/products/detail/vishay-dale/CMF55500R00FEBF/3621957)
		- [220kΩ](https://www.digikey.ca/en/products/detail/yageo/HHV-25FR-52-220K/2813166?utm_adgroup=&utm_source=google&utm_medium=cpc&utm_campaign=PMax%20Product_High%20ROAS%20Categories&utm_term=&productid=2813166&utm_content=&utm_id=go_cmp-20222745078_adg-_ad-__dev-c_ext-_prd-2813166_sig-CjwKCAiAyp-sBhBSEiwAWWzTns__4Uw7cd1UtiOjPPkdBOCdrPLYicKkpt88y9yRfUM-bWR8RxSWixoCBuYQAvD_BwE&gad_source=1&gclid=CjwKCAiAyp-sBhBSEiwAWWzTns__4Uw7cd1UtiOjPPkdBOCdrPLYicKkpt88y9yRfUM-bWR8RxSWixoCBuYQAvD_BwE)



## Isolated Power Supply Components
(This is a possible configuration - not final)
- [TSM1212S 12v to 12v converter](https://www.digikey.ca/en/products/detail/traco-power/TSM-1212S/9383729) (This is to isolate the 12v power needed on both the HV and LV sides)
-  [1 µf cap](https://www.digikey.ca/en/products/detail/kemet/C0805C105M3REC7210/19187599?utm_adgroup=Kemet&utm_source=google&utm_medium=cpc&utm_campaign=PMax%20Shopping_Supplier_Kemet&utm_term=&productid=19187599&utm_content=Kemet&utm_id=go_cmp-17861998787_adg-_ad-__dev-c_ext-_prd-19187599_sig-CjwKCAiAp5qsBhAPEiwAP0qeJiifoK9KTxF9DXGEaa5OqBMW5vinpKY3If_sfeC92sSJIbInDmQ2IhoCUGYQAvD_BwE&gad_source=1&gclid=CjwKCAiAp5qsBhAPEiwAP0qeJiifoK9KTxF9DXGEaa5OqBMW5vinpKY3If_sfeC92sSJIbInDmQ2IhoCUGYQAvD_BwE)
- - [Diode](https://www.digikey.ca/en/products/detail/onsemi/S1D/3042696?utm_adgroup=&utm_source=google&utm_medium=cpc&utm_campaign=PMax%20Supplier_Focus%20Supplier&utm_term=&productid=3042696&utm_content=&utm_id=go_cmp-20282403582_adg-_ad-__dev-c_ext-_prd-3042696_sig-CjwKCAiAp5qsBhAPEiwAP0qeJonW0WY0irg5tw_UcS6X8UwN435r5AoQ38GqCtuH2LHngi-wNt56DBoChUsQAvD_BwE&gad_source=1&gclid=CjwKCAiAp5qsBhAPEiwAP0qeJonW0WY0irg5tw_UcS6X8UwN435r5AoQ38GqCtuH2LHngi-wNt56DBoChUsQAvD_BwE)
- J1 Connector 6-pin Connector for Power in and LED output
	Inputs:
		GLV Input from Car (+/-)
		Positive Voltage for Red LED (+/-)
		Positive Voltage for Green LED (+/-)

 
