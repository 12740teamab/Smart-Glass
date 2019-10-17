# Smart Cup
TONG LEI; SHULIN LIU; JIARONG XIE
<p> </p>
[Video](http://)
<p> </p>
<p><a href="http://12740teamab.github.io/Smart-Glass/Final Report.pdf" target="_blank">Final Report</a></p>
<p> </p>
<p><a href="http://12740teamab.github.io/Smart-Glass/Progress Report.pdf" target="_blank">Progress Report</a></p>

<h2>Introduction</h2>
<p>Smart cup aims to provide people a way to live a healthier life. With a special monitoring system, smart cup can track the water consumption of user and calculate the average water consumption in a specific period. If the average water consumption is below the recommended value, smart glass will gently remind user to drink more water. At the same time, smart cup can show the water temperature to make sure that user drinks the water with appropriate temperature. Besides, smart cup has a special liquid classification system to make sure user is drinking “real” water instead of unhealthy soft drink. Last, smart cup can also detect and show the environment temperature and humidity.<p>

<p align="center">
  <img width="350" height="350" src="https://user-images.githubusercontent.com/55921083/67034688-2414d480-f0e6-11e9-97ee-6e5d0da9ff7d.jpg">
</p>
<p align="center">Figure 1: Smart Cup</p>

<h3>Motivation</h3>
<p>•	Health authorities commonly recommend eight 8-ounce glasses per day<p>
<p>•	A typical adult naturally loses about 2-3 liters of water per day<p>
<p>•	Benefits of drinking water:</p>
<p>-	Lubricates the joints</p>
<p>-	Forms saliva and mucus</p>
<p>-	Regulates body temperature</p>
<p>-	Helps maintain blood pressure</p>
<p>-	Prevents kidney damage</p>

<p align="center">
  <img width="330" height="200" src="https://user-images.githubusercontent.com/55921083/66975160-9eecd980-f06b-11e9-8691-c6ac8e0c60d3.png">
</p>
<p align="center">Figure 2: Benefits of Drinking Water</p>

<h3>Goals</h3>
<p>•	Remind people to drink sufficient water</p>
<p>•	Remind people to drink healthy water instead of soft drinks</p>
<p>•	Remind people whether the water is ready to drink with appropriate temperature</p>

<h2>Methodology</h2>
<h3>Phenomena of Interest</h3>
<p>•	Measure the weight of the cup to get the amount of liquid in the cup</p>
<p>•	Measure the time to calculate the hourly water consumption</p>
<p>•	Measure the light intensity at the bottom of the cup to get the types of liquid</p>
<p>•	Measure the temperature of the water to make sure it is comfortable to drink</p>
<p>•	Measure the temperature and humidity of environment</p>

<h3>Sensors Used</h3>
<p>•	Weight Sensor: HX711</p>
<p>   -	Bracket diameter: 10CM</p>
<p>   -	Working voltage: 5V or 3.3V</p>
<p>   -	Test weight: 5KG</p>
<p>   -	Height: 3.5cm (including column)</p>
<p>   -	AD module: HX711 (24-bit high-precision A/D conversion chip HX711)</p>
<p>   -	Operating temperature range: -20 degrees - +85 degrees</p>
<p>   -	Accuracy after calibration: less than 1g</p>

<p align="center">
  <img width="200" height="200" src="https://user-images.githubusercontent.com/55921083/67034913-94bbf100-f0e6-11e9-942c-fdeac1015fad.jpg">
</p>

<p>•	Light Sensor: LM393</p>
<p>   -	Input Voltage: 3.3V to 5V</p>
<p>   -	Dimension: 15mm x 33mm x 8mm</p>
<p>   -	Weight: 4 gm</p>
<p>   -	Signal output indicator light</p>
<p>   -	LDR module 4 PIN</p>
<p>   -	Able to detect ambient brightness and light intensity Adjustable sensitivity</p>

<p align="center">
  <img width="200" height="200" src="">
</p>

<p>•	Temperature Sensor: DS18B20</p>
<p>   -	Operating voltage: 3V to 5V</p>
<p>   -	Temperature Range: -55°C to +125°C</p>
<p>   -	Accuracy: ±0.5°C</p>
<p>   -	Output Resolution: 9-bit to 12-bit (programmable)</p>
<p>   -	Unique 64-bit address enables multiplexing</p>
<p>   -	Conversion time: 750ms at 12-bit </p>
<p>   -	Available as To-92, SOP and even as a waterproof sensor</p>

<p align="center">
  <img width="200" height="200" src="">
</p>

<p>•	Temperature and Humidity Sensor: DHT11</p>
<p>   -	Measurement Range: 20-90% RH, 0-50°C</p>
<p>   -	Humidity Accuracy: +/- 5% RH</p>
<p>   -	Temperature Accuracy: +/- 2°C</p>
<p>   -	Resolution: 1</p>
<p>   -	Package: 4 Pin Single Row</p>

<p align="center">
  <img width="200" height="200" src="">
</p>

<h3>Logic Flow Chart</h3>
<p align="center">
  <img width="891" alt="Screen Shot 2019-10-16 at 10 31 55 PM" src="https://user-images.githubusercontent.com/55921083/66975782-95fd0780-f06d-11e9-8596-2ca518a9333c.png">
</p>
<p align="center">Figure 3: Logic Flow Chart</p>

<h2>Experienments and Results</h2>
<h4>First Meeting</h4>
<p>•	Make sure the types of sensors that we need, including a pressure sensor (HX711, ordered through Amazon), a temperature sensor (in box), a light sensor (in box)</p>
<p>•	Make a prototype “smart-cup” with only temperature sensor and light sensor (pressure sensor is on the way)</p>
<p>•	Connect multiple sensors to Raspberry Pi, and organize the python code to show the output of sensors correctly</p>
<p>•	With test, we make sure that the light sensor can detect the change of light density while changing the liquid above it from coffee into pure water. We also confirm that the temperature can detect the temperature of liquid in glass</p>
<p>•	Implement the design details of “smart-cup”, including the placement of sensors, data that we need to set up a range for different types of liquid, method to prevent the effect of light outside the glass</p>

<h4>Second Meeting</h4>
<p>In this meeting, we tried to figure out whether we could use water level sensor to detect the volume of liquid in bottle. We designed an experiment. We added specific volume of water into the cup at a time with a water level sensor, then kept adding. We tried to find the linear relationship between the volume of water and water-level sensor output voltage. But just like the Figure 4 showing below, we did not find a relationship between these two variables. After water depth achieving 2 cm, the voltage kept staying at 1.8. Thus, based on this experiment, we held the view that water level sensor was not a good choice for smart cup.</p>

<p align="center">
  <img width="500" height="300" src="">
</p>
<p align="center">Figure 4: Water Level Sensor Voltage Output vs. Water Depth</p>

<h4>Third Meeting</h4>
<p>•	We made a model of the smart cup and placed all sensors in it.</p>
<p>•	Weight sensor calibration: at first, the output of the weight sensor was just a huge number which would decrease when we put more weight on it. Thus, we used a set of standard weights to do calibration on it, transferring its unit to ‘g’. The standard weights include 4 standard weights of 0.5 lb, 10 standard weights of 10 g. Different combinations of them were used to obtain as many as data points. For each weight, relatively stable sensor reading out was collected for about half a minute. The average of these data was used as the reading for calculation. R was used for processing the data. A linear model between the sensor reading and the actual weigh was assumed and regressed. The result is shown in Figure 6.  The slope of the line is -0.00283, the intercept is 23460. (weight = -0.00283*output + 23460)</p>

<p align="center">
  <img width="300" height="350" src="">
</p>
<p align="center">Figure 5: Weight Sensor Calibration</p>

<p align="center">
  <img width="500" height="300" src="">
</p>
<p align="center">Figure 6: Weight Sensor Output Value vs. Actual Weight</p>

<p>•	We deigned an experiment to find out the threshold for light sensor to tell the difference between water and non-water liquid: we put the light sensor at the bottom of the cup and a LED light source on top. Then we put water and other soft drink in cup each time, recorded the output value of the light sensor. From the results in Figure 9, it is easy to find the difference among water and other soft drink. We set the threshold as 1.</p>

<p align="center">
  <img width="300" height="350" src="">
</p>
<p align="center">Figure 7: Types of Soft Drink</p>

<p align="center">
  <img width="300" height="350" src="">
</p>
<p align="center">Figure 8: Running a Drink Type Test</p>

<p align="center">
  <img width="500" height="300" src="">
</p>
<p align="center">Figure 9: Light Sensor Output vs. Different Types of Liquid</p>

<p>•	Wrote a python code in Raspberry Pi, which was used to control the smart cup and upload the water consumption record to OpenChirp.</p>

<p align="center">
  <img width="700" height="300" src="">
</p>
<p align="center">Figure 10: Non-Water Consumption from OpenChirp</p>

<p align="center">
  <img width="700" height="300" src="">
</p>
<p align="center">Figure 11: Water Temperature from OpenChirp</p>

<p align="center">
  <img width="700" height="300" src="">
</p>
<p align="center">Figure 12: Results on Terminal</p>

<h4>Final Experiment</h4>
<p>After finishing all parts of this smart cup, we conducted an experiment on it. At the beginning, there was 195 ml water in the cup. Then we drank 135ml water. After that, we drank the rest of the water and poured 300ml unclear soft drink in it. Next, we drank 200 ml soft drink. Then we drank the rest of them couple minutes later. The timeseries results from OpenChirp exactly match our experiment.</p>

<p align="center">
  <img width="700" height="600" src="">
</p>
<p align="center">Figure 13: Timeseries Results from OpenChirp</p>

<h2>Discussion</h2>
<p>This project provides us an opportunity to put the knowledge that we learn from class into practice:</p>
<p>•	In this project, we use four different sensors: light sensor, weight sensor, temperature sensor and temperature & humidity sensor. During this project, we learn how to connect multiple sensors to the Raspberry Pi. Based on what we learn from course, we use different GPIO interfaces of Pi. Then we use python code to read data from sensors based on the number of those interfaces.</p>

<p>•	We use OpenChirp to upload and visualize the water consumption record. It is the first time that we use IOT. We hold the view that IOT makes the transition of data between different devices much more convenient. The embed visualization function also provides us an efficient way to find the pattern of data.</p>

<p>•	With collecting data from sensors, calibration and sending commands to the actuator, we become familiar with the complete circle of using sensors. In a word, we know how to use sensors to design a product.</p>

<p>Although we spent a plenty of time on this smart cup, it is still not perfect. We can make a better version if we have more time and higher budget. For example, we only use the light sensor to tell if the liquid is water or not for now. But if we have enough sensors, we can buy more sensors and collect more information about the liquid, which could help us make better prediction about the type of the liquid.</p>

<p>This project also improves our ability to find problems and solve them. During this project, we met different kinds of problems. For example, we found the output of weight sensor was not stable with unpattern fluctuation one day. After checking, we found that we used the same GPIO interface for two sensors, which may arise some signal confliction. Thus, we used another interface to fix it.</p>

<p>Thanks to the assistance of Professor Mario and TAs, their help and patience make us finish this project successfully.</p>

<h2>Reference</h2>
<p>[1] https://www.healthline.com/nutrition/how-much-water-should-you-drink-per-day</p>
<p>[2] https://www.amazon.com/TeOhk-Electronic-Digital-Converter-Breakout/dp/B07SX2MYMX/ref=sr_1_9?keywords=hx711&qid=1571273390&sr=8-9</p>
<p>[3] http://kookye.com/2016/08/01/smart-home-sensor-kit-for-arduinoraspberry-pi/</p>
<p>[4] https://robu.in/product/lm393-photosensitive-light-dependent-control-sensor-module/</p>
<p>[5] https://components101.com/sensors/ds18b20-temperature-sensor</p>
<p>[6] https://www.mouser.com/datasheet/2/758/DHT11-Technical-Data-Sheet-Translated-Version-1143054.pdf</p>
