- **Camera Module** : The camera module will capture images or videos of the railway track and surrounding areas to detect wildlife presence.

- **5G Module** (RxTxSemi 5G USB Modem Kit): The 5G module enables real-time communication between the IoT device and the main train control center, allowing for fast data transfer and decision-making.

- **Edge Computing Module** (Raspberry pi 4 - 4GB RAM): This module processes video feeds and machine learning models in real-time, reducing latency and enabling faster detection of wildlife presence.

- **Sensors** : Additional sensors can be used to detect other factors such as weather conditions, temperature, or soil moisture, which might affect wildlife behavior.

**Required Sensors:**

|Sensor|Function|Default I2C Address|Address Range (Configurable)|
|---|---|---|---|
|**BME280**|Temp/Hum/Pressure|**0x77** (or 0x76)|0x76 to 0x77|
|**BH1750**|Light (Lux)|**0x23**|0x23 or 0x5C|
|**TSL2561**|Infrared/Visible|**0x39**|0x29, 0x39, or 0x49|

for we use 12V lithium phosphate battery rechargeable 
Buck Converter 24V/12V to 5V 5A Power Module DC-DC XY-3606 Power Converter


