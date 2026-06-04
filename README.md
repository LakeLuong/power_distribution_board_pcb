# power_distribution_board_pcb
Custom KiCad power distribution PCB that takes in +48V and regulates it down to 5V, 3.3V and 12V through two adjustable Lm760660 buck converters and a Tps62913. I made this for a bigger project I am working on for an underwater FPV drone to power different components such as ESCs which will take in +48V, sensors which takes 3.3V and 5V for my raspberry pi, and 12V for cameras. 

<img width="1176" height="593" alt="image" src="https://github.com/user-attachments/assets/77dabe71-1442-477a-8b46-69e010ff298b" />

<img width="1026" height="457" alt="image" src="https://github.com/user-attachments/assets/99375eac-02f7-4890-ac9f-a425fd3a10e0" />


BOM: 

Tps62913	Low current buck converter converting 5V to 3.3V	2	$5.52		

Lm70660	High Current Buck Converter that takes 48V and brings it down to 12V and 5V	2	$13.60		

0805 4mOhm resistors	Current-sense resistors	10	$5.57	

0805 54.9k Ohm resistors	resistor connects from RT to AGND, helps with switching frequency	10	$0.37	

0806 20.5kOhm resistors	En Vulo resistors	10	$0.34	

0805 3.24kOhm resistor	Compensation capacitor for lm760660	10	$0.34	

0805 1 Ohm resistor	Bootstrap resistor	10	$0.51

0805 2.49kOhm resistor	feedback divider resistor	10	$0.34	

0805 4.87kOhm resistor	Feedback divider resistor	10	$0.34		

0805 52.3kOhm resistor	S-CONF resistor	10	$0.34	

0805 31.6kOhm resistor	Resistor divider for feedback	10	$0.58	

0805 100kOhm resistor	UVLO resistor, pull up resistors, etc, to control current flow	25	$0.64		

2.2uH inductor	Stores energy during switching and smooths current	3	$6.61	

Ferrite Bead	Blocks high frequency noise	5	$1.55	

0805 470nF Ceramic Capacitor	Reduce low frequency output noise on the Tps62913	10	$1.24	

0806 0.1uF Ceramic Capacitor	High frequency bypass capacitors	10	$1.07

0805 0.1uF Ceramic Capacitor	Decouples VDDA analog bias rail	10	$0.72	

0805 4.7uF Ceramic Capacitor	bypass/decoupling capacitor for VCC	5	$1.60	

0805 22uf Ceramic Capacitor	Smooths output voltage	10	$3.74	

1210 47uF Ceramic Capacitors	Smooths output voltage from regulator	15	$8.42	

0805 10uF Ceramic Capacitors	Input capacitors to provide short bursts of current to regulator	10	$3.48		

1210 4.7 uF Ceramic Capacitors	Input capacitors to provide short burst of current	10	$8.49		

0805 150pf Ceramic Capacitors	Compensation capacitors, helps buck converter stay stable from high frequency noise	10	$0.85		

1210 22uF Ceramic Capacitor	Gives high frequency noise to GND	10	$4.77

0805 10nF Ceramice Capacitors	bypass and filtering + provide positive power supply through VCC	10	$0.60	

0805 0.047 uF Ceramic Capacitor	Boostrap capacitor for buck converter	10	$1.47	

0805 2200pF SMD Ceramic Capacitor	Decoupling and filtering for 5v rail	10	$0.39	
