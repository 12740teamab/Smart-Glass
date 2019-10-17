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

![IMG_1065](https://user-images.githubusercontent.com/55921083/66975041-284fdc00-f06b-11e9-81c7-36b61a8c7980.jpg)

<h3>Motivation</h3>
<p>•	Health authorities commonly recommend eight 8-ounce glasses per day<p>
<p>•	A typical adult naturally loses about 2-3 liters of water per day<p>
<p>•	Benefits of drinking water:</p>
<p>-	Lubricates the joints</p>
<p>-	Forms saliva and mucus</p>
<p>-	Regulates body temperature</p>
<p>-	Helps maintain blood pressure</p>
<p>-	Prevents kidney damage</p>

<img width="310" alt="WechatIMG62" src="https://user-images.githubusercontent.com/55921083/66975160-9eecd980-f06b-11e9-8691-c6ac8e0c60d3.png">

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

![51UjB-VAY3L _SL1000_](https://user-images.githubusercontent.com/55921083/66975382-597cdc00-f06c-11e9-916e-19afb1867ab5.jpg)

<p>•	Light Sensor: LM393</p>
<p>   -	Input Voltage: 3.3V to 5V</p>
<p>   -	Dimension: 15mm x 33mm x 8mm</p>
<p>   -	Weight: 4 gm</p>
<p>   -	Signal output indicator light</p>
<p>   -	LDR module 4 PIN</p>
<p>   -	Able to detect ambient brightness and light intensity Adjustable sensitivity</p>

![14](https://user-images.githubusercontent.com/55921083/66975509-b24c7480-f06c-11e9-934f-d07274db6b38.jpg)

<p>•	Temperature Sensor: DS18B20</p>
<p>   -	Operating voltage: 3V to 5V</p>
<p>   -	Temperature Range: -55°C to +125°C</p>
<p>   -	Accuracy: ±0.5°C</p>
<p>   -	Output Resolution: 9-bit to 12-bit (programmable)</p>
<p>   -	Unique 64-bit address enables multiplexing</p>
<p>   -	Conversion time: 750ms at 12-bit </p>
<p>   -	Available as To-92, SOP and even as a waterproof sensor</p>

![9](https://user-images.githubusercontent.com/55921083/66975691-43235000-f06d-11e9-9617-8b282db2ef43.jpg)

<p>•	Temperature and Humidity Sensor: DHT11</p>
<p>   -	Measurement Range: 20-90% RH, 0-50°C</p>
<p>   -	Humidity Accuracy: +/- 5% RH</p>
<p>   -	Temperature Accuracy: +/- 2°C</p>
<p>   -	Resolution: 1</p>
<p>   -	Package: 4 Pin Single Row</p>

![10](https://user-images.githubusercontent.com/55921083/66975744-76fe7580-f06d-11e9-94b2-c13c0e95a4b5.jpg)

<h3>Logic Flow Chart</h3>
<img width="891" alt="Screen Shot 2019-10-16 at 10 31 55 PM" src="https://user-images.githubusercontent.com/55921083/66975782-95fd0780-f06d-11e9-8596-2ca518a9333c.png">

<h2>Experienments and Results</h2>
<p>Describe the experiments you did and present the results; Use tables and plots if possible</p>

<h2>Discussion</h2>
<p>This project provides us an opportunity to put the knowledge that we learn from class into practice:</p>
<p>•	In this project, we use four different sensors: light sensor, weight sensor, temperature sensor and temperature & humidity sensor. During this project, we learn how to connect multiple sensors to the Raspberry Pi. Based on what we learn from course, we use different GPIO interfaces of Pi. Then we use python code to read data from sensors based on the number of those interfaces.</p>

<p>•	We use OpenChirp to upload and visualize the water consumption record. It is the first time that we use IOT. We hold the view that IOT makes the transition of data between different devices much more convenient. The embed visualization function also provides us an efficient way to find the pattern of data.</p>

<p>•	With collecting data from sensors, calibration and sending commands to the actuator, we become familiar with the complete circle of using sensors. In a word, we know how to use sensors to design a product.</p>

<p>Although we spent a plenty of time on this smart cup, it is still not perfect. We can make a better version if we have more time and higher budget. For example, we only use the light sensor to tell if the liquid is water or not for now. But if we have enough sensors, we can buy more sensors and collect more information about the liquid, which could help us make better prediction about the type of the liquid.</p>

<p>This project also improves our ability to find problems and solve them. During this project, we met different kinds of problems. For example, we found the output of weight sensor was not stable with unpattern fluctuation one day. After checking, we found that we used the same GPIO interface for two sensors, which may arise some signal confliction. Thus, we used another interface to fix it.</p>

<p>Thanks to the assistance of Professor Mario and TAs, their help and patience make us finish this project successfully.</p>

<h2>Reference</h2>
<p>[1]https://www.healthline.com/nutrition/how-much-water-should-you-drink-per-day</p>
<p>[2]https://www.amazon.com/TeOhk-Electronic-Digital-Converter-Breakout/dp/B07SX2MYMX/ref=sr_1_9?keywords=hx711&qid=1571273390&sr=8-9</p>
<p>[3]http://kookye.com/2016/08/01/smart-home-sensor-kit-for-arduinoraspberry-pi/</p>
<p>[4]https://robu.in/product/lm393-photosensitive-light-dependent-control-sensor-module/</p>
<p>[5]https://components101.com/sensors/ds18b20-temperature-sensor</p>
<p>[6]https://www.mouser.com/datasheet/2/758/DHT11-Technical-Data-Sheet-Translated-Version-1143054.pdf</p>
