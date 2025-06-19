 # 🌡️ Digital Twin for Room Temperature Monitoring using NodeMCU and DHT11

This project implements a digital twin system for periodically monitoring room temperature using the NodeMCU microcontroller and DHT11 temperature sensor. The collected data is logged into Excel sheets for real-time analysis and record-keeping.


## Project Overview

- Hardware Used: NodeMCU (ESP8266), DHT11 Temperature & Humidity Sensor
- Data Logging: Temperature readings are collected at regular intervals and logged into Excel.
- Purpose: To monitor and track room temperature conditions accurately and consistently.

## Features

- Reads temperature (and humidity) data from the DHT11 sensor
- Sends the data from NodeMCU to a connected system via serial or Wi-Fi
- Logs data periodically into an Excel file for tracking and visualization
- Works as a basic **Digital Twin** representation of the real-world room environment


##  Components Required

| Component        | Description                          |
|------------------|--------------------------------------|
| NodeMCU (ESP8266)| Microcontroller with Wi-Fi capability|
| DHT11            | Temperature & Humidity Sensor        |
| Jumper Wires     | For connections                      |
| Breadboard       | For prototyping                      |
| Computer         | To run logging script (Python/Excel) |


##  Circuit Diagram

- DHT11 to NodeMCU:
  - VCC → 3.3V
  - GND → GND
  - DATA → D4 (GPIO2)

##  Installation & Setup

1. Connect Hardware
   - Wire the DHT11 sensor to the NodeMCU as per the circuit diagram.

2. Upload Code
   - Use Arduino IDE to upload the code to NodeMCU.
   - Libraries needed:
     - `DHT.h`
     - `ESP8266WiFi.h` (optional if sending over Wi-Fi)

3. Logging Data
   - If using Serial + PLX-DAQ:
     - Open Excel with PLX-DAQ macro
     - Select the correct COM port and start logging
   - If using Python script:
     - Ensure `pyserial`, `openpyxl` are installed
     - Run the script to receive serial data and log into Excel


## Sample Output

| Timestamp           | Temperature (°C) | Humidity (%) |
|---------------------|------------------|---------------|
| 2025-06-19 10:00:00 | 27.3             | 58.2          |
| 2025-06-19 10:05:00 | 27.6             | 57.9          |


##  Future Improvements

- Add Wi-Fi-based cloud logging (e.g., Firebase, Thingspeak, or Google Sheets)
- Visualize data in a web dashboard
- Add threshold-based alerts using buzzer or notifications
- Integrate with home automation system



