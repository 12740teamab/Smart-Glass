# Smart-Glass
TONG LEI;SHULIN LIU;JIARONG XIE

<h3>Introduction</h3>
<p>Smart glass aim to provide people healthier lifestyle. With a special monitor system, small glass can track the water consumption of owner and calculate the average water consumption in a specific period. If the average water consumption is below the recommended value, smart glass would gently remind you to drink more water. At the same time, smart glass can show the temperature to make sure you drink the water with appropriate temperature. Last but not least, small glass has a special liquid classification system to make sure you are drinking “real” water instead of unhealthy soft drink.<p>
  
<h3>Motivation</h3>
<p>• Health authorities commonly recommend eight 8-ounce glasses<p>
<p>• A typical adult naturally loses about 2-3 liters of water a day<p>
<p><b>Benefit of drinking water:</b></p>
<p>• Lubricates the joints</p>
<p>• Forms saliva and mucus</p>
<p>• Regulates body temperature</p>
<p>• Helps maintain blood pressure</p>
<p>• Prevents kidney damage</p>

<h3>Goals</h3>
<p>• Remind people of drinking sufficient water</p>
<p>• Remind people of drinking healthy</p>
<p>• Remind people if the water is ready to drink with appropriate</p>

<h2>For Progress Report</h2>
<h3>Current Progress</h3>
<p>• Make sure the type of sensors that we need, including a pressure sensor(HX711, ordered through Amazon), a temperature sensor(in box), a light sensor(in box)</p>
<p>• Make a prototype “smart-glass” with only temperature sensor and light sensor(pressure sensor is on the way)</p> 
<p>• Connect multiple sensors to Raspberry Pi, and organize the python code to show the output of sensors correctly</p>
<p>• With test, we make sure that the light sensor can detect the change of light density while changing the liquid above it from coffee into pure water. We also confirm that the temperature can detect the temperature of liquid in glass</p>
<p>• Implement the design details of “smart-glass”, including the placement of sensors, data that we need to set up a range for different types of liquid, method to prevent the effect of light outside the glass</p>

<h3>Problems Encountered</h3>
<p>• How to connect another sensor to Raspberry Pi? Using the same ADC or another one?</p>
<p>• Current experiments show the lighting sensor can differentiate cola and water with same ambient light level. However, ambient light can be a main noise that cannot be ignored in future experiments. How to eliminate the impact of ambient lighting?</p>
<p>• The measurement of temperature delays, which cannot indicate the real-time temperature of water in the glass.</p>

<h3>Future Plan</h3>
<p>• Connect the weight sensor to Raspberry Pi and obtain its measurement</p>
<p>• Appropriately configure all sensors in a container</p>
<p>• Conduct more experiments to figure out how to differentiate types of several common drinks, such as cola, orange juice, and coffee</p>
<p>• Solve the temperature measurement delay problem (by adding a light source and blocking the ambient light)</p>
<p>• Figure out the ways to remind people</p>
<p>• Complete all codes</p>
<p>• Test</p>
<p>• Connect all sensors to OpenChirp (if time allows)</p>

<h2>Methodology</h2>
<h3>Phenomena of Interest</h3>
<p>Describe the physical phenomena of interest, e.g. physical principles, static and dynamic behavior, and signal characteristics</p>

<h3>Sensors Used</h3>
<p>Describe the sensors you used, e.g. physical principles, static and dynamic behavior, and signal characteristics</p>
<p>• Weight Sensor: HX711</p>
<p>• Light Sensor: LM393</p>
<p>• Temperature Sensor: DS18B20</p>

<h3>Signal Conditioning and Processing</h3>
<p>Describe the signal conditioning and processing procedures</p>

<h2>Experienments and Results</h2>
<p>Describe the experiments you did and present the results; Use tables and plots if possible</p>

<h2>Discussion</h2>
<p>Discuss the insights from the project</p>
