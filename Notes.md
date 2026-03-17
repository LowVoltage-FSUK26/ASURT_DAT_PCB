\- Faraday Cage for ESP / Hardware hacking of esp with an external antenna.

\- Separate Data lines of (ADC, SPI, I2C, CAN, etc..)

\- Search about ground loops (Not a problem, there are no return paths for signals)

\- Configure PCB planes **\*\*\*\*\*\*\*\*\*\*\*DONE\*\*\*\*\*\*\*\*\*\*\***

\- Which is better (two GND planes) or (one for GND and one for Power) **\*\*\*\*\*\*\*\*\*\*\*DONE\*\*\*\*\*\*\*\*\*\*\***
- Which power plane we will choose? (which 3.3V?) (Is it better to do the double GND planes?) **\*\*\*\*\*\*\*\*\*\*\*DONE\*\*\*\*\*\*\*\*\*\*\***
(Two GND Planes)

\- Configure the DFM for JLC PCB **\*\*\*\*\*\*\*\*\*\*\*DONE\*\*\*\*\*\*\*\*\*\*\***

\- Impedance and Length matching for the SD-Card SDIO (Search for a way to measure trace Impedance and tune it) **\*\*\*\*\*\*\*\*\*\*\*DONE\*\*\*\*\*\*\*\*\*\*\***

\- Consider I2C Interface Capacitance (Search for a way to measure and tune trace Capacitance)

\- Find a solution for the Temperature sensor I2C wiring (I2C Adapter? 100m extension) (Discuss with Samy) **\*\*\*\*\*\*\*\*\*\*\*DONE\*\*\*\*\*\*\*\*\*\*\***
(I2C to CAN PCB)

\- Review the Buck converter's values (remeasure the current and decide whether we will use a module or design a new one) (Discuss with Samy)

* Luckily, All Buck Components have the same size as the Old Buck Converter, so it is backword compatible.

\- Discuss with Samy and Ziad about how can we get the desired components (LCSC or Locally) **LCSC\*\*\*\*\*\*\*\*\*\*\*\*
\*\*\*\*\*\*\*\*\*\*\*DONE\*\*\*\*\*\*\*\*\*\*\***

\- Add a Coin cell Battery (Choose a good battery and find its Altium footprint) (Configure VBAT on the STM32F4) (Add a 100nF decoupling cap on the VBAT) **\*\*\*\*\*\*\*\*\*\*\*DONE\*\*\*\*\*\*\*\*\*\*\***

\- Place the CAN Transceivers near to the 34-pin Connector **\*\*\*\*\*\*\*\*\*\*\*DONE\*\*\*\*\*\*\*\*\*\*\***

\- VIAs should be at least 0.15mm (preferred) larger than Via hole size. **\*\*\*\*\*\*\*\*\*\*\*DONE\*\*\*\*\*\*\*\*\*\*\***

\- Seka placed too many GND VIAs that are not used (even under the GPS sensor), why is that? (Search)

* Coin Cell, SD Card, Decoupling Caps down. **\*\*\*\*\*\*\*\*\*\*\*DONE\*\*\*\*\*\*\*\*\*\*\***
* Resized the PCB to 10\*10 cm^2 and placed the 34-pin connector in the same place as the old DAQ for backword compatibility. **\*\*\*\*\*\*\*\*\*\*\*DONE\*\*\*\*\*\*\*\*\*\*\***

\- 2oz or 1oz copper? chose 1oz for now **\*\*\*\*\*\*\*\*\*\*\*DONE\*\*\*\*\*\*\*\*\*\*\***

* GPS module measurements needed (28.055m) **\*\*\*\*\*\*\*\*\*\*\*DONE\*\*\*\*\*\*\*\*\*\*\***
* Add Mounting Holes for IMU and GPS
* Add Labels for each pin in the 3-pin headers and push buttons
* Check the Layer Stack from the JLC-PCB
* **\*\*\*\*\*\*\*\*\*\*\*IMPORTANT:** when routing ESP CAN 3v3, route provide different routes for both the shifter and non shifter modes
* Hmmmmm The heat sink is connected to ground...... right? LOL



###### New To-Do List:

* GPS headers
* ESP new package
* ESP repositioning (antenna issues)
* Q1 \& Q2
* Designators



Optional: 

* SPI between ESP and STM

