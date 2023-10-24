# RFID and Fingerprint Scanner Integration on ESP8266

This README provides an overview and instructions for the project that combines an RFID (Radio-Frequency Identification) module with a fingerprint scanner using the MFRC522 RFID module and the Adafruit Fingerprint sensor. The project runs on an ESP8266 controller.

## Project Overview

The project's goal is to create a secure access control system that uses both RFID cards and fingerprint scanning for user authentication. Users can scan an RFID card or place their fingerprint on the sensor for access.

### Key Components
- **MFRC522 RFID Module**: This module reads RFID cards for user authentication.
- **Adafruit Fingerprint Sensor**: This sensor captures and verifies fingerprints for user authentication.
- **ESP8266 Controller**: The ESP8266 is the microcontroller responsible for managing the integration of the RFID and fingerprint scanner modules.
- **SoftwareSerial Library**: The project utilizes the SoftwareSerial library for communication with the fingerprint sensor.

## Getting Started

To set up the project, follow these steps:

### Hardware Setup
1. Connect the MFRC522 RFID module to the ESP8266 controller according to your wiring configuration.
2. Connect the Adafruit Fingerprint sensor to the ESP8266 controller.

### Software Setup
1. Make sure you have the required libraries installed for the MFRC522 module and Adafruit Fingerprint sensor.
2. Upload the project code to the ESP8266 controller using the Arduino IDE or your preferred development environment.
3. After uploading the code, open the Arduino IDE Serial Monitor.

## Usage

The project offers two primary modes: RFID card scanning and fingerprint scanning.

1. **RFID Card Scanning (`SYS_SCAN_MODE`)**
   - Activate this mode to scan an RFID card.
   - The system reads the card's UID and validates it.
   - If the card is valid, access is granted (`SYS_ACCESS_GRANT`), and the UID is printed.
   - If the card is invalid, access is denied (`SYS_ACCESS_DENID`).

2. **Fingerprint Scanning (`SYS_PROG_MODE`)**
   - Activate this mode to enroll fingerprint data.
   - The system guides the user through placing their fingerprint on the sensor.
   - If the enrollment is successful, the system prints "Enrolled" and the assigned ID.
   - If the enrollment fails, the system prints "Failed to Store."

3. **Flush Fingerprint Data (`SYS_FLSH_FPS`)**
   - This command flushes all stored fingerprint data.

4. **Get RFID Data (`SYS_GET_RFID`)**
   - Activate this mode to read an RFID card's UID.
   - The system reads the card's UID and prints it.

### Troubleshooting
- Make sure the RFID and fingerprint sensor modules are correctly connected to the ESP8266 controller.
- Be mindful of power requirements for the modules and their compatibility with the ESP8266.

