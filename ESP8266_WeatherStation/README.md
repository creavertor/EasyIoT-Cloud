# ESP8266 Weather Station

A comprehensive weather monitoring station for ESP8266 that reads temperature and humidity data from a DHT22 sensor and sends it to EasyIoT Cloud via REST API.

## Features

- Temperature monitoring (Celsius and Fahrenheit)
- Humidity monitoring (%)
- WiFi connectivity
- Automatic data reporting to EasyIoT Cloud
- Configurable reporting interval

## Hardware Requirements

- ESP8266 board (e.g., NodeMCU, Wemos D1 Mini)
- DHT22 temperature and humidity sensor
- Connecting wires

## Wiring

Connect DHT22 sensor to ESP8266:
- DHT22 VCC -> ESP8266 3.3V
- DHT22 GND -> ESP8266 GND
- DHT22 Data -> ESP8266 GPIO2 (D4 on NodeMCU)

## Configuration

Before uploading, update the following in the code:

1. WiFi credentials:
   - `AP_SSID` - Your WiFi network name
   - `AP_PASSWORD` - Your WiFi password

2. EasyIoT Cloud parameters:
   - `EIOT_CLOUD_TEMP_INSTANCE_PARAM_ID` - Temperature parameter ID from EasyIoT Cloud
   - `EIOT_CLOUD_HUM_INSTANCE_PARAM_ID` - Humidity parameter ID from EasyIoT Cloud

3. Optional settings:
   - `REPORT_INTERVAL` - Data reporting interval in seconds (default: 60)
   - `DHT22_PIN` - GPIO pin connected to DHT22 data pin (default: 2)

## Required Libraries

- ESP8266WiFi (included with ESP8266 board support)
- DHT - Available at: https://github.com/iot-playground/EasyIoT-Cloud/tree/master/libraries/DHT

## Usage

1. Install the required libraries
2. Update configuration parameters in the code
3. Upload to your ESP8266 board
4. Open Serial Monitor at 115200 baud to view status messages
5. Monitor your weather data on EasyIoT Cloud at http://cloud.iot-playground.com

## Serial Output

The sketch outputs weather data to the serial console:
```
=== Weather Station ===
Status  Humidity (%)  Temperature (C)  (F)
OK      55.2          22.3             72.1
```

## More Information

Visit http://iot-playground.com for more details and support.
