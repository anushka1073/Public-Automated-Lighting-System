# Public-Automated-Lighting-System
Public lightings are often lit even during daytime resulting in the wastage of energy and exorbitant maintenance costs. Currently we have a manual system where the street lights will be switched ON in the evening before sunset and switched OFF the next morning. In some areas, there has been a shift towards timer control for the on-off of public lighting. However, this has not been very effective because the actual timing for these lights to be switched ON is when there is absolute darkness and turned OFF when there is sufficient daylight, the accuracy of which cannot be timer controlled and requires manual interference. 

### Solution
This project aims at designing and implementing an IoT based Public Lighting System which resolves the hurdle of electrical power wastage and eliminates the manual operation factor in the system. Our proposed IoT based system’s core functionality lies in its ability to sense ambient light using LDRs placed strategically near the street lights and IR sensors which detect objects in the vicinity of the street light. We are extending this project by adding one more constraint that the Street light will only glow if there is darkness AND if someone is passing by, hence further reducing power consumption by glowing the streetlight only when required. 
In this project we are demonstrating the prototype of the Smart Street Light with 3 IR sensors, 1 LDR sensor and 3 LEDs - each representing one street light. We are also updating the LDR sensor data to ThingSpeak, which is a cloud-based platform used to send and receive the data in real time. Using this, we can control the LEDs (Street lights) over the internet. 

### Hardware Components-
<li>ESP8266 NodeMCU</li>
<li>Micro USB cable</li>
<li>LEDs</li>
<li>Jumper wires</li>
<li>IR sensors</li>
<li>LDR sensors</li>

### Software Components
<li>Arduino IDE</li>
<li>Thingspeak</li>

### Circuit Diagram

<img alt= "image" src= "https://github.com/Chinthachowdeswari/Automatic_street_light/blob/main/Circuit-Diagram-for-IoT-based-Smart-Street-Light.png?raw=true">

### Working Cases
<li>Case 1: When there is daylight and a vehicle passes by</li>
In this case although the IR sensor detects the object in the vicinity, since there is enough light intensity falling on the LDR, the LED does not turn ON.

<img alt="image" src= "https://drive.google.com/file/d/18wSaQ8zCFPJsrjoXYgXGx608MwezCMEB/view?usp=sharing">

<li>Case2: When it is dark and no vehicle passes by</li>
In this case although it is dark, since no vehicle is passing by, The LED will not turn on in order to reduce power consumption.
Case3: When it is dark and a vehicle passes by
<li>In this final case, since it is both dark and an object is being detected, the led will turn on thus working as an intelligent streetlight</li><br>

Finally, we have uploaded our LDR and IR data to ThingSpeak to analyse the operation of the sensor to monitor it over the internet

### Future Enhancements
<li>	Currently when it is dark but no vehicle is detected, the LED is not turned on but we aim to keep the light on at all times at 40% efficiency in the dark and increase the efficiency to 100% when vehicles pass by so that streets remain lit in the dark even for pedestrians and small entities which may or may not be detected by the IR sensor</li>
<li> Change the power source to Solar Panels for a greener alternative</li>
<li> Utilize sensor data sent to ThingSpeak to study Traffic Patterns which will help in efficient city planning</li>
