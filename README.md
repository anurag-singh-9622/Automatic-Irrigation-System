# Automatic-Irrigation-System
Providing water to the plants automatically without going in the fields. Getting information like Soil moisture, Humidity, temperature around plants.

“AUTOMATIC IRRIGATION SYSTEM WITH SOLAR POWER”

A 
PBL PROJECT 
ON
 “Bachelor of Technology”
In
“Electronics and Communication engineering”

ANURAG KUMAR SINGH         18SECE1030031
SUNNY CHAURASHIA               19SECE1030005
 SAURABH SINGH                       18SECE1030032
VISHWANATH GUPTA             19SECE1030002

Under the Guidance of
Dr. ROHIT TRIPATHI
 
GALGOTIAS UNIVERSITY
GREATER NOIDA
 
 
School of Electronics and Communication Engineering

CERTIFICATE

This is to Certified that this project report of “AUTOMATIC IRRIGATION SYSTEM WITH SOLAR POWER”is submitted by “ANURAG KUMAR SINGH, SUNNY CHAURASIA, SAURABH SINGH, VISHWANATH GUPTA” who carried out the PBL Work under my supervision. I approve this project for submission of the Bachelor of Technology in the School of Electrical, Electronics & Communication Engineering. Galgotias University.




Prof. B . Mohapatra                  Prof. Rohit Tripathi                  Prof. Rohit Tripathi

(P.C., SECE)                           (PBL Coordinator)                            (Project Mentor)

 




ABSTRACT
Now a days its a challenge to improve development of plant in respect of its growth and to reduce costs which leads to an innovative idea of using an automated irrigation system which will further help in better management of water and human resources. An automated irrigation system have been developed using sensors technology with Arduino to efficiently utilize water for irrigation purpose. The system has soil moisture sensor inserted into the soil of the plants and a water level sensor placed in a water container from where water will be pumped to plants for irrigation. An algorithm has been build out with threshold values of soil moisture sensor to control the water quantity in soil and also a water level sensor has been implemented to measure the water level in tank. This project requires Arduino board having inbuilt ATMega328 microcontroller. This project is need of the hour to convert manual irrigation into an automated irrigation which with the help of soil moisture sensor will detect dankness content of soil leading to turn ON/OFF of pumping motor. Human efforts can be reduced using this technique and increase saving of water by efficiently irrigating the plants. The design has been made with better resource management and low power consumption. This project brings into play a micro-controller which is of 8051 family, this programmable micro-controller collects the input signals converted into values of moisture in the soil via soil moisture sensors. As the microcontroller starts obtaining the signals, it creates an output that forces a relay for running the water pumping motor. An LCD screen is also linked to the micro-controller to show moisture conditions of the soil and water pump. The water level sensor is used to detect the level of tank so that tank contains efficient water to transfer into crops.
 
ACKNOWLEDGEMENT
It gives me immense pleasure to express my deepest sense of gratitude and sincere thanks to my highly respected and esteemed guide Dr. Rohit Tripathi (ECE DEPT.) Galgotias University for their valuable guidance, encouragement, and help for completing this work. Their useful suggestions for this whole work and co-operative behaviors are sincerely acknowledged. I would like to express my sincere thanks to Dr. Priestly Shan Dean, Galgotias University, for providing me this opportunity to undertake this project. I also wish to express my gratitude to Prof. B. Mohapatra(Program Chair) (SECE) for his kindhearted support. I am also grateful to my teacher Dr. Rohit Tripathi Their constant support and guidance. I also wish to express my indebtedness to my parents as well as my family member whose blessings and support always helped me to face the challenges ahead. In the end, I would like to express my sincere thanks to all my friends and others who helped me directly or indirectly during this project work.

Place: GALGOTIAS UNIVERSITY
Date:

           ANURAG KUMAR SINGH                                         (18SECE1030031)

          SUNNY CHAURASIA                                                  (19SECE1030005)

          SAURABH SINGH                                                        (18SECE1030032)

          VISHWANATH GUPTA                                               (19SECE1030002)


 
TABLE OF CONTENTS

TITLE PAGE……………………………….…………………………………………...	1
CIRTIFICATE…………………………….………….……………………………….…	2
ABSTRACT…………………………………………………………………………..….	3	
ACKNOWLEDGEMENT………………….………………………………….…….…..	4
TABLE OF CONTENTS………………….………………………………………..…....	5
LIST OF TABLES……………………………………………………………………….	6
LIST OF FIGURES……………………………………………………………………...	7
LIST OF SYMBOLS………………………………………………………………….…	8
LIST OF PRICES……………………………………………………………….……….	9
CHPTER-1 INTRODUCTION………………….…………………………………........	10
                (1.1) INTRODUCTION TO PROJECT……………………………………...	11
                (1.2) INTRODUCTION TO IRRIGATION SYSTEM…………..…………..	12
                (1.3) WORKING…………………………………………………………..……	13
CHAPTER-2 PROJECT DETAILS……………………………………………………..	14
                (2.1) BLOCK DIAGRAM…………………………………………………..….	15
                (2.2) CIRCUIT DIAGRAM……………………………………………………	16
                (2.3) COMPONENT DETAILS……………………………………………….	17
                (2.4) PROGRAM CODE………………………………………………………	23
CHAPTER-3 CONCLUSION……………………………………………………………	24
                 (3.1) CONCLUSION………………………………………………………..….	25
                 (3.2) CLOSURE……………………………………………………………..…	26
                 (3.3) USES……………………………………………………………………	26
                 (3.4) REFERENCES…………………………………………………………	27
                      
LIST OF TABLES
TABLE NO.                                                       DESCRIPTION
1.	                                                   Price of components 
2.	                                                   List of symbols
3.	                                                  Arduino specifications


















LIST OF FIGURES
FIGURE NO.                                            DESCRIPTION
1.	                                                        Arduino
2.	                                                        Soil Moisture Sensor
3.	                                                        DHT 11
4.	                                                        Battery 9v
5.	                                                        Rechargeable Battery
6.	                                                        Relay
7.	                                                        Motor
8.	                                                        Solar panel
9.	                                                        Tank
10.	                                                        Pot
11.	                                                        Bread Board
12.	                                                        Connecting Wires











LIST OF SYMBOLS
SR.NO. 					NAMES 					SYMBOLS
1.	                                                   Resistance                                                     Ω
2.	                                                   Capacitance                                                   C
3.	                                                   Frequency                                                     Hz
4.	                                                   Power                                                            W
5.	                                                   Voltage                                                          V
















TABLE OF PRICES
COMPONENTS	PRICES
ARDUINO	350
SOIL MOISTURE SENSOR	80
DHT 11	110
BATTERY 9V	20
RECHARGEBLE BATTERY	250
RELAY	70
MOTOR	40
SOLAR PANNEL	400
TANK	20
POT	60
BREAD BOARD	50
CONNECTING WIRES	60
TOTAL	1520



















CHAPTER – 1
INTRODUCTION









1.1.  INTRODUCTION  TO PROJECT
The main aim of this project was to provide water to the plants or gardening automatically using microcontroller (Arduino Uno). We can automatically watering the plants when we are going on vacation or don’t we have to bother my neighbors, Sometimes the neighbors do too much of watering and the plants end up dying anyway. There are timer based devices available in India which waters the soil on set interval. They do not sense the soil moisture and the ambient temperature to know if the soil actually needs watering or not.
 Assimilation is that the artificial application of water to the land or soil It is used to assist in the growing of agricultural crops, maintenance of landscapes, and re vegetation of disturbed soils in dry areas and during periods of inadequate rainfall. When a zone comes on, the water flows through the lateral lines and ultimately finally ends up at the irrigation electrode (drip) or mechanical device heads. Several sprinklers have pipe thread inlets on the lowest of them that permits a fitting and also the pipe to be connected to them. The sprinklers are usually used in the top of the head flush with the ground surface. 
As the method of dripping will reduce huge water losses it became a popular method by reducing the labor cost and increasing the yields. When the components are activated, all the components will read and gives the output signal to the controller, and the information will be displayed to the user (farmer). The sensor readings are analog in nature so the ADC pin in the controller will convert the analog signals into digital format. Then the controller will access information and when the motors are turned On/Off it will be displayed on the LCD Panel, and serial monitor windows. There are many systems are available to water savings in various crops, from basic ones to more technologically advanced ones. For instance, in one system plant watering status was monitored and irrigation scheduled based on temperature presents in soil content of the plant.



1.2. INTRODUCTION TO IRRIGATION SYSTEM
Freshwater is needed for crop and energy production, industrial fabrication as well as human and ecosystem needs. According to AQUASTAT database (AQUASTAT, 2016), 69% of the total extracted freshwater is used by agriculture sector, whereas 19% is used by industrial sector and the rest in used by domestic segment. Therefore, water can be considered as a critical need in agriculture sector for future global food security However, continued increase in demand for water by domestic and industrial sectors and greater concerns for environmental quality have create a challenge to every country to reduce the farm water consumption and sustain the fresh food requirement (Flörke et al., 2013). Consequently, there is an urgent need to create strategies based on science and technology for sustainable use of water. Industrialist and researchers are working to build efficient and economic automatic systems to control water usage in order to reduces much of the wastage. Irrigation is an artificial application of watering the land for agricultural production. The requirement of water to the soil depends on soil properties such as soil moisture and soil temperature. Effective irrigation can influence the entire growth process and automation in irrigation system using modern technology can be used to provide better irrigation management. In general, most of the irrigation systems are manually operated. These traditional techniques can be replaced with automated techniques of irrigation in order to use the water efficiently and effectively. Conventionally, farmers will present in their fields to do irrigation process. Nevertheless, nowadays farmers need to manage their agricultural activity along with other occupations. A sensor based automated irrigation system provides promising solution to farmers where the presence of a farmer in field is not compulsory during irrigation process.






1.3. WORKING
An automatic plant watering system using Arduino microcontroller UNO R3 is programmed such that it gives the interrupt signals to the motor via the motor driver module. Soil sensor is connected to the A0 pin to the Arduino board which senses the moisture content present in the soil. Whenever the soil moisture content values goes down, the sensor senses the humidity change, giving signal to the microcontroller so that the pump (motor) can be activated. This concept can be used for automatic plant watering system. The circuit comprises an Arduino UNO board, a soil moisture sensor, a 5V motor pump, a Motor driver L293D (IC1), motor driver IC to run the water pump. You can power the Arduino board using a 5V to 9V wall wart or plugin adaptor or solar panel. You need a separate 5V to 9v battery for the pump motor.



















CHAPTER-2
PROJECT DETAILS









2.1. BLOCK DIAGRAM



 










2.2. CIRCUIT DIAGRAM

 




2.3. COMPONENT DETAILS
2.3.1. ARDUINO UNO
In figure 1 it is showing an Arduino board is an open source platform used for building electronics projects. Arduino is a programmable circuit’s board which we can write a program based on your projects. Arduino program will be uploading with IDE (Integrated Development Environment) software that runs on your computer, it is used to write and upload computer code to the Arduino physical board. Arduino language is merely a set of C/C++ functions that can be called from your code.
 
 
Figure 1: ARDUINO UNO
2.3.2. SOIL MOISTURE SENSOR
o	Operating voltage: 3.3V~5V
o	Dual output mode, analog output more accurate
o	Having LM393 comparator chip, stable
o	Panel PCB Dimension: Approx.3cm x 1.5cm
o	Soil Probe Dimension: Approx. 6cm x 3cm
o	Cable Length: Approx.21cm
o	DO: digital output interface(0 and 1)
 
2.3.3. DHT 11 
•	To detect humidity, the DHT11 measures the electrical resistance between two electrodes. 
•	To measure air temperature, the device uses a surface mounted (SMT) NTC temperature sensor, or a thermistor. Thermistors are variable resistors that change resistance based on the temperature. This thermistor’s resistance will decrease when the temperature increases.
 

2.3.4. BATTERY 9V
•	It is used to provide power to Arduino. 
•	It is 9v battery. 
 
2.3.5. RECHARGEABLE BATTERY
•	This battery is connected to Water Pump motor to provide power to work.
•	This battery is rechargeable so that we are applying solar panel to recharge battery.
 
2.3.6. RELAY
A relay driver IC is an electromagnetic switch that will be use when ever we want to use a low voltage circuit to switch a motor ON and OFF .
o	High current relay, AC250V 10A , DC30V 10A
o	2 LEDs to indicate when relays are ON
o	Works on logic level signals from 3.3V or 5V devices
o	Opto isolation circuitry
o	PCB size: 50x45mm
 
Figure 2: Relay
2.3.7. WATER PUMP MOTOR
•	Working voltage: DC 6-12V
•	Working crrenr: 0.5-0.7A
•	Recommended voltage ratings are 9v 1A or 12v 1A
•	The maximum head range of 3m.
•	Works with liquid upto 80°C
•	The maximum flow rate of up to 1 – 3L/min.
 
2.3.8. SOLAR PANEL
•	DC voltage output       12V
•	Max Power output       10W
•	NO. of cells                  36
•	Panel Dimensions         410 X 395 X 23mm
•	 Weight                         2.1Kg
•	Material                         POLYCRYSTALLINE SILICON
 

2.3.9. WATER TANK
•	It is used to store water.
•	when needed water motor pump can suck water from it.
 
2.3.10. FLOWER POT
•	It is used in this project to demonstrate the watering system.
 



2.3.11. BREAD BOARD
 
2.3.12. CONNECTING WIRES
 









2.4. PROGRAM CODE
 














CHAPTER-3
CONCLUSION   











3.1. CONCLUSION
Thus the “Automated Irrigation system based on soil moisture using Arduino” has been designed and tested successfully. It has been developed by integrated features of all the hardware components used. 
Presence of every module has been reasoned out and placed carefully, thus contributing to the best working of the unit. Thus, the Arduino Based Automatic Plant Watering System has been designed and tested successfully . The system has been tested to function automatically. The moisture sensors measure the moisture level (water content) of the different plants. 
If the moisture level is goes to be below the desired and limited level, the moisture sensor sends the signal to the Arduino board which triggers the Water Pump to turn ON and supply the water to respective plant using the Rotating Platform/Sprinkler. When the desired moisture level is reached, the system halts on its own and the water Pump is turned OFF. Thus, the functionality of the entire system has been tested thoroughly and it is said to function successfully.












3.2. CLOSUER
The main purpose of this chapter is to propose an automated irrigation system that water the plant without any human control. The automated irrigation system implemented is found to be feasible and cost effective for optimizing water resources for agricultural production. 
Besides the automated irrigation system, the proposed system also provides the monitoring function where users are able to check the soil moisture based on the reading on the LCD display. The proposed system has been designed and tested to function automatically.
 For future works, the automated irrigation system can be configured to measure the moisture level (water content) according to the moisture requirement of the different plants.

3.3. USES
•	This system automatically operate motor to provide required amount of water to plants.
•	This is solar powered system so that it is less costly than dc power supply.
•	It measure the soil moisture content, temperature , and humidity so that farmer can deduce the climatic condition of his field.
•	With the use of  this system we can save vast amount of water.
•	This system is very cheap and convenient in compare to Regular motor pump system.
•	It can be used in all type of farming.
•	It can be used for garden irrigation system.
•	Town parks.
•	Remote area farming




3.4. REFERENCES
Books and Journals


1.	Agrawal, N., & Singhal, S. (2015). Smart drip irrigation system using raspberry pi
          and arduino. International Conference on Computing, Communication & 
         Automation, 928–932. http://doi.org/10.1109/CCAA.2015.7148526

2.	Devika, S. V, Khamuruddeen, S., Khamurunnisa, S., Thota, J., & Shaik, K. (2014).
         Arduino Based Automatic Plant Watering System. International Journal of
        Advanced Research in Computer Science and Software Engineering, 4(10), 449–456

3.	Flörke, M., Kynast, E., Bärlund, I., Eisner, S., Wimmer, F., & Alcamo, J. (2013). Domestic
         and industrial water uses of the past 60 years as a mirror of socio-economic
        development: A global simulation study. Global Environmental Change, 23(1),
        144–156. http://doi.org/10.1016/j.gloenvcha.2012.10.018

4.	Kumar Sahu, C., & Behera, P. (2015). A low cost smart irrigation control system. In
          2nd International Conference on Electronics and Communication Systems,
          ICECS 2015 (pp. 1146–1151). http://doi.org/10.1109/ECS.2015.7124763

