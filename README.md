# Day 9: Ultrasonic Distance Dashboard

This project uses an ESP32 and an HC-SR04 ultrasonic sensor to measure distance. The ESP32 hosts a web page that refreshes automatically to show the latest reading.

## Components

- ESP32 DevKit v1
- HC-SR04 ultrasonic distance sensor

## Connections

- HC-SR04 VCC → ESP32 5V
- HC-SR04 GND → ESP32 GND
- HC-SR04 TRIG → ESP32 GPIO 5
- HC-SR04 ECHO → ESP32 GPIO 18

> For a physical ESP32, the HC-SR04 ECHO pin outputs 5 V. Use a voltage divider or level shifter so the ESP32 GPIO receives 3.3 V or less. Wokwi simulation wiring may not require this.

## Wokwi Simulation

[Run the simulation](https://wokwi.com/projects/476576837145321473)

## How to use

1. Start the Wokwi simulation.
2. Open the Serial Monitor and note the ESP32's IP address.
3. Open that address in a browser that can reach the simulation.
4. The dashboard refreshes to show the measured distance.

## How it works

The ESP32 sends a trigger pulse to the HC-SR04, measures the echo pulse duration, calculates the distance, and serves the latest value on a web page.
