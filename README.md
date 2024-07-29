# Intoxi-Lock Alcohol Detection and Engine Locking System

## Overview

Intoxi-Lock is an IoT-based project designed to enhance vehicle safety by preventing drunk driving. The system detects the presence of alcohol in the driver's breath and automatically stops the vehicle if alcohol is detected. This feature is exclusively targeted at the driver, ensuring that only the driver’s alcohol level is monitored.

## Table of Contents
- [Introduction](#introduction)
- [Features](#features)
- [Components](#components)
- [Setup and Installation](#setup-and-installation)
- [Usage](#usage)
- [Team](#team)
- [License](#license)

## Introduction

Driving under the influence of alcohol is a leading cause of road accidents. Intoxi-Lock aims to reduce these incidents by implementing a system that can detect alcohol levels in the driver and disable the vehicle if the levels are above a predefined limit. This project uses an Arduino UNO as the central controller, combined with various sensors and components, to create an efficient alcohol detection and engine locking mechanism.

## Features

- **Alcohol Detection**: Uses an MQ3 sensor to detect alcohol levels in the driver's breath.
- **Engine Locking System**: Automatically stops the vehicle if alcohol is detected.
- **Driver-Specific Detection**: Ensures that the detection is focused on the driver.
- **Visual and Audible Alerts**: Alerts the driver with LEDs and a buzzer if alcohol is detected.

## Components

1. **Arduino UNO**: The microcontroller board that acts as the brain of the system, controlling all other components.

2. **MQ3 Sensor**: A gas sensor specifically designed to detect alcohol. It provides an analog output based on the concentration of alcohol in the air.

3. **B.O. Motor**: Used to simulate the vehicle's engine in this prototype setup.

4. **Transistors (BC547)**: NPN transistors used for switching and controlling the motor and other components.

5. **Resistors (220 Ohm x2)**: Used to limit current and protect components, particularly the LEDs and transistors.

6. **5V Relay**: An electrically operated switch used to control the B.O. motor (engine) based on the alcohol detection result.

7. **Buzzer**: Provides an audible alert when alcohol is detected.

8. **Switch**: Allows the driver to manually override the system in case of false positives.

9. **Patch Cords**: Used for connecting different components in the circuit.

10. **Battery**: Powers the entire system.

11. **LEDs**: Indicate the system's status and alert the driver when alcohol is detected.

## Setup and Installation

1. **Wiring the Components**:
    - Connect the MQ3 sensor to the Arduino's analog input.
    - Connect the B.O. motor to the 5V relay, controlled by a transistor connected to the Arduino.
    - Attach the buzzer, LEDs, and switch to the respective digital pins on the Arduino.
    - Use resistors to protect the LEDs and transistors.

2. **Programming the Arduino**:
    - Write and upload the code to the Arduino UNO, using the MQ3 sensor to read alcohol levels and control the relay and buzzer based on the readings.

3. **Powering the System**:
    - Connect the battery to power the Arduino and other components.

## Usage

Once the system is set up, it continuously monitors the alcohol level in the driver's breath. If the alcohol concentration exceeds the predefined limit, the system will:
1. Trigger the buzzer and LED alert.
2. Activate the relay to cut off power to the B.O. motor (engine), effectively stopping the vehicle.

The driver can use the switch to override the system if necessary, though this is recommended only in cases of false positives.

## Team (All from the same dept. Electronics & Inst. Engg.)

This project was developed as a group effort by:
- Smarak Patra
- Deepak Sahu
- Saurabh Rawat
- Pritam Prakash
- Bijaya Ketan Mahapatra

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
