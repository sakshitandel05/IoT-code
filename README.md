# Smart Waste Sorter using Arduino

This project is a simple smart waste management system using Arduino. It is designed to detect and sort waste into **wet** and **dry** categories based on moisture level. It uses an ultrasonic sensor to detect the presence of waste and a soil moisture sensor to determine the type of waste. A servo motor is used to physically sort the waste into appropriate bins.

# Components used:
* Arduino Uno 
* Ultrasonic Sensor (HC-SR04)
* Soil Moisture Sensor (Analog)
* Servo Motor (SG90 or equivalent)
* Breadboard and jumper wires

# How It Works

1. The ultrasonic sensor detects the presence of waste by measuring distance.
2. If an object is within a defined range, the soil moisture sensor is activated.
3. Moisture readings are collected and averaged.
4. If the moisture level is above a certain threshold, the waste is classified as **wet**, otherwise as **dry**.
5. The servo motor rotates accordingly to sort the waste into the correct bin.
6. After sorting, the servo motor resets to its original position.

# Moisture Calibration

The project uses `maxDryValue = 1` as the threshold for deciding between dry and wet waste.
The soil sensor readings are mapped and constrained for consistent behavior.
The system averages multiple readings to reduce error.

# Code Overview

* The main code is written in Arduino C/C++.
* `pulseIn()` is used to read distance from the ultrasonic sensor.
* `analogRead()` is used to measure moisture values.
* The servo motor is controlled using the `Servo` library and responds to the moisture condition.

# How to Run

1. Connect all components as per the circuit.
2. Upload the `.ino` file to the Arduino board using the Arduino IDE.
3. Open the Serial Monitor to view sensor values and waste classification.
4. Test the system by placing different types of waste in front of the ultrasonic sensor.

# Future Improvements

 Add visual indicators like LEDs or a display screen
 Use a more precise moisture sensor
 Extend the project to include IoT features (e.g., data logging, cloud integration)
 Create a physical bin system with multiple compartments


