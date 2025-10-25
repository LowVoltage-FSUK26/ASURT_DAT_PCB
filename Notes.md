\- Faraday Cage for ESP / Hardware hacking of esp with an external antenna.

\- Separate Data lines of (ADC, SPI, I2C, CAN, etc..)

\- Search about ground loops 

\- Configure PCB planes **\*\*\*\*\*\*\*\*\*\*\*DONE\*\*\*\*\*\*\*\*\*\*\***

\- Which is better (two GND planes) or (one for GND and one for Power) **\*\*\*\*\*\*\*\*\*\*\*DONE\*\*\*\*\*\*\*\*\*\*\***

\- Configure the DFM for JLC PCB **\*\*\*\*\*\*\*\*\*\*\*DONE\*\*\*\*\*\*\*\*\*\*\***

\- Configure SPI between ESP and STM32F4

\- Impedance and Length matching for the SD-Card SDIO (Search for a way to measure trace Impedance and tune it)

\- Consider I2C Interface Capacitance (Search for a way to measure and tune trace Capacitance)

\- Find a solution for the Temperature sensor I2C wiring (I2C Adapter? 100m extension) (Discuss with Samy)

\- Review the Buck converter's values (remeasure the current and decide whether we will use a module or design a new one) (Discuss with Samy)

\- Discuss with Samy and Ziad about how can we get the desired components (LCSC or Locally)

\- Add a Coin cell Battery (Choose a good battery and find its Altium footprint) (Configure VBAT on the STM32F4) (Add a 100nF decoupling cap on the VBAT) **\*\*\*\*\*\*\*\*\*\*\*DONE\*\*\*\*\*\*\*\*\*\*\***

\- Place the CAN Transceivers near to the 34-pin Connector

\- VIAs should be at least 0.15mm (preferred) larger than Via hole size.





\- 2oz or 1oz copper? chose 1oz for now

