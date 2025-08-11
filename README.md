           =================================================================================================================
                                      EV-Battery-Level-Indicator-Using-ATtiny85-7-Segment-Display
           =================================================================================================================
----------------------
Project Description:
----------------------
This project monitors and displays the voltage level of an electric vehicle (EV) battery using a 
microcontroller-based setup.The  system uses analog voltage sampling, voltage regulation,
and a 74HC595 shift register to drive a 7-segment LED display, all  designed and tested using KiCad.

---------------
Components:
---------------
1. ATtiny85 microcontroller
2. LM7805 Voltage Regulator
3. 74HC595 Shift Register
4. 7-Segment LED Display
5. Voltage Divider Circuit
6. 12V Battery
7. Resistors

---------------
Tools Used:
---------------
KiCad (Schematic, PCB, Gerber, BOM)

-----------------
Pin Connections:
-----------------
ATtiny85 → 74HC595

ATtiny85 Pin	          Function	           74HC595 Pin
PB1 (Pin 6)	           Data (MOSI)	        DS (Pin 14)
PB2 (Pin 7)	           Clock (SCK)	        SH_CP (Pin 11)
PB0 (Pin 5)	           Latch	              ST_CP (Pin 12)

1. ATtiny85 PB3 (Pin 2) → Voltage divider output (Analog input).
2. 74HC595 Q0-Q6 → 7-Segment Display segments (with resistors).
3. Common pin of 7-Segment → VCC (Common Anode) or GND (Common Cathode).
4All grounds connected together.
----------------
How it works:
----------------
12Volts Battery
     |
     v
Voltage Regulator (LM7805): Converts 12V to 5V
     |
     v
Voltage Divider: Scales the battery voltage
     |
     v
Micro controller (ATtiny85): Reads voltage and calculates battery level
     |
     v
Shift register (74HC595): Send data to display
     |
     v
7-Segment display: Shows battery level

---------------
Step Process:
---------------
1. Power Supply – The circuit is powered from the EV’s 12V battery.
2. Voltage Regulation – LM7805 converts 12V down to a stable 5V for all components.
3. Voltage Sensing – A resistor divider scales the battery voltage for safe measurement.
4. Voltage Measurement – ATtiny85 reads voltage via ADC.
5. Battery Level Calculation – The microcontroller maps voltage to battery percentage/level.
6. Data Output – Battery level is sent to 74HC595 shift register.
7. Display – The 7-segment display shows the calculated battery level.
------------
Notes:
------------
1. Adjust voltage divider resistor values according to your battery voltage range.
2. Always use resistors for each display segment to prevent damage.


