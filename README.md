#Patient Health Monitoring System (Arduino + ESP8266 + ThingSpeak)

#Introduction

This project is a real-time patient health monitoring system that measures Heart Rate (BPM) and Body Temperature using Arduino and sends the data to the ThingSpeak IoT cloud via an ESP8266 WiFi module. The system uses a Pulse Sensor and Temperature Sensor, displays live readings on an LCD display, and uploads data to the cloud for remote monitoring.

It is designed to be a low-cost, IoT-enabled solution for healthcare applications such as patient monitoring, telemedicine, and health analytics.

#Features

LCD Display → Shows live BPM and temperature values.

Pulse Sensor Integration → Detects heartbeat in real time.

Temperature Sensor → Monitors patient body temperature.

LED Indicators → Blinks/fades with heartbeat detection.

IoT Connectivity → Uses ESP8266 WiFi module to send data.

ThingSpeak Cloud Integration → Stores and visualizes health data online.

Dual Code Setup → Arduino collects and processes data; ESP8266 handles WiFi and cloud upload.

Scalable & Open Source → Can be extended with more sensors (SpO2, ECG, etc.).

#How to Run

1. Hardware Required

Arduino UNO / Nano

ESP8266 WiFi Module

Pulse Sensor (for BPM)

LM35 / similar analog Temperature Sensor

16x2 LCD with I2C module

LEDs and basic jumper wires


2. Software Setup

1. Install Arduino IDE (latest version).


2. Install the following libraries:

LiquidCrystal_I2C.h

SoftwareSerial.h

ThingSpeak.h

ESP8266WiFi.h



3. Create a ThingSpeak account and a new channel with:

Field 1 → BPM

Field 2 → Temperature

Copy your Channel ID and Write API Key.


3. Upload the Code

Step 1: Upload the Arduino code (patient_monitor.ino) to Arduino.

Step 2: Upload the ESP8266 WiFi code (wifi_module.ino) to ESP8266 (via NodeMCU / Serial flasher).

Step 3: Update your WiFi SSID, password, and API key inside both codes.



4. Run the System

1. Power up the Arduino and ESP8266.


2. LCD will display BPM and Temperature in real-time.


3. Data will be uploaded automatically to ThingSpeak every 15 seconds.


4. Open your ThingSpeak channel to view graphs and analytics of health parameters.# IoT-embedded-projects
