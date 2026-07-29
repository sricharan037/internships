# Task 2: Sensor-Based Simulation - IoT Radar System

## Project Title
**Ultrasonic Radar System using Arduino**

## Overview
This project simulates a real-time **Radar System** using an Ultrasonic Sensor, a Servo Motor, and an OLED Display. The system continuously sweeps its environment using the servo motor and detects objects using the HC-SR04 sensor. The detected distance is rendered on the OLED screen and visualized in a radar-like graphical interface.

The simulation was developed, wired, and tested entirely on **Wokwi**, an advanced browser-based Arduino and IoT simulator.

## Components Used (Virtual)
- Arduino Uno
- HC-SR04 Ultrasonic Sensor
- MG90S Servo Motor
- SSD1306 OLED Display (128x64)

## Working Principle
1. The Servo Motor continuously rotates in a sweeping motion from 0° to 180°.
2. At each incremental position, the Ultrasonic Sensor measures the distance to any reflective object in front of it.
3. The measured distance and the current angle are processed by the Arduino.
4. A radar-like visual sweep and numeric distance are displayed dynamically on the OLED screen.

## Project Files
- **Source Code**: [`sketch.ino`](./sketch.ino) containing the full Arduino logic for sensor integration and OLED rendering.
- **Circuit Diagram**: [`circuit.png`](./task2(1).png) (or refer to the image files in this directory).
- **Simulation Platform**: [Wokwi Online Simulator](https://wokwi.com/projects/467178708278498305)

## How to Run the Simulation
1. Open the [Wokwi Project Link](https://wokwi.com/projects/467178708278498305).
2. Click the **Play** button to initialize the Arduino.
3. Observe the servo movement and interact with the ultrasonic sensor to see real-time distance readings on the OLED display.
