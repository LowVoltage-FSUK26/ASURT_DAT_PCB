\- Faraday Cage for ESP / Hardware hacking of esp with an external antenna.

\- Separate Data lines of (ADC, SPI, I2C, CAN, etc..)

\- Search about ground loops (Not a problem, there are no return paths for signals)

\- Configure PCB planes **\*\*\*\*\*\*\*\*\*\*\*DONE\*\*\*\*\*\*\*\*\*\*\***

\- Which is better (two GND planes) or (one for GND and one for Power) **\*\*\*\*\*\*\*\*\*\*\*DONE\*\*\*\*\*\*\*\*\*\*\***
\- Which power plane we will choose? (which 3.3V?) (Is it better to do the double GND planes?)

\- Configure the DFM for JLC PCB **\*\*\*\*\*\*\*\*\*\*\*DONE\*\*\*\*\*\*\*\*\*\*\***

\- Configure SPI between ESP and STM32F4

\- Impedance and Length matching for the SD-Card SDIO (Search for a way to measure trace Impedance and tune it)

\- Consider I2C Interface Capacitance (Search for a way to measure and tune trace Capacitance)

\- Find a solution for the Temperature sensor I2C wiring (I2C Adapter? 100m extension) (Discuss with Samy)

\- Review the Buck converter's values (remeasure the current and decide whether we will use a module or design a new one) (Discuss with Samy)
* Luckily, All Buck Components have the same size as the Old Buck Converter, so it is backword compatible.

\- Discuss with Samy and Ziad about how can we get the desired components (LCSC or Locally) **LCSC\*\*\*\*\*\*\*\*\*\*\*\***

\- Add a Coin cell Battery (Choose a good battery and find its Altium footprint) (Configure VBAT on the STM32F4) (Add a 100nF decoupling cap on the VBAT) **\*\*\*\*\*\*\*\*\*\*\*DONE\*\*\*\*\*\*\*\*\*\*\***

\- Place the CAN Transceivers near to the 34-pin Connector **\*\*\*\*\*\*\*\*\*\*\*In Progress\*\*\*\*\*\*\*\*\*\*\***

\- VIAs should be at least 0.15mm (preferred) larger than Via hole size.

\- Seka placed too many GND VIAs that are not used (even under the GPS sensor), why is that? (Search)

* Coin Cell, SD Card, Decoupling Caps down.
* 8\*15 cm^2 (Probably we will not do it)
* Resized the PCB to 10\*10 cm^2 and placed the 34-pin connector in the same place as the old DAQ for backword compatibility.
* Placed the 2 CAN Transceivers infront of each other so that when we connect them to the CAN BUS we will use VIAs to allign the traces to the pins.


\- 2oz or 1oz copper? chose 1oz for now **\*\*\*\*\*\*\*\*\*\*\*DONE\*\*\*\*\*\*\*\*\*\*\***

* GPS module measurements needed (28.055m)
* Add Mounting Holes for IMU and GPS
* Add Names for each pin in the 3-pin headers
* **\*\*\*\*\*\*\*\*\*\*\*IMPORTANT:** when routing ESP CAN 3v3, route provide different routes for both the shifter and non shifter modes
