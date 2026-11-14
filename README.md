# 🚗 Hand Gesture Controlled Car Using ESP32 and MPU6050

## 📌 Project Overview

The Hand Gesture Controlled Car is a wireless robotic vehicle that can be controlled through hand movements. The project uses an MPU6050 Inertial Measurement Unit (IMU) sensor to detect hand orientation and an ESP32 microcontroller to process the sensor data and transmit control commands wirelessly.

A second ESP32 receives these commands and controls the movement of the vehicle through motor drivers connected to four DC motors.

The vehicle uses four Mecanum wheels, enabling multidirectional movement based on the motor control commands.

## 🎯 Project Aim

To design and develop a wireless Hand Gesture Controlled Car using ESP32 microcontrollers and an MPU6050 IMU sensor. The objective is to control the movement and direction of a four-wheel robotic vehicle through hand gestures without requiring a conventional remote controller.

## 🛠️ Apparatus Used

### Hardware Components

| S.No | Component | Quantity |
|---|---|---|
| 1 | ESP32 Development Board | 2 |
| 2 | MPU6050 IMU Sensor | 1 |
| 3 | L298N Motor Driver | 2 |
| 4 | DC Motors | 4 |
| 5 | Mecanum Wheels | 4 |
| 6 | Breadboard | 1 |
| 7 | Battery Source | 1 |
| 8 | Jumper Wires | As Required |

### Software Requirements

- Arduino IDE
- ESP32 Board Manager
- I2Cdev Library
- MPU6050 Library

## ⚙️ Working Principle

The project operates using two main sections:

### 1. Transmitter Section

- The MPU6050 sensor is connected to the first ESP32 microcontroller.
- The sensor detects hand orientation and movements using its accelerometer and gyroscope.
- The ESP32 reads the sensor data through I2C communication.
- Based on the detected hand movements, corresponding control commands are generated.
- These commands are transmitted wirelessly to the receiver ESP32.

### 2. Receiver Section

- The second ESP32 acts as the receiver.
- It receives the wireless control commands from the transmitter.
- Based on the received commands, the ESP32 generates control signals for the motor drivers.
- Two L298N motor drivers control the four DC motors.
- The four Mecanum wheels enable the vehicle to move in different directions.

## 🔌 Circuit Connections

### 1. MPU6050 with ESP32 (Transmitter)

The MPU6050 communicates with the ESP32 using the I2C communication protocol.

| MPU6050 Pin | ESP32 Pin |
|---|---|
| VCC | 3.3V |
| GND | GND |
| SDA | GPIO 21 |
| SCL | GPIO 22 |

### 2. ESP32 with Motor Drivers (Receiver)

The receiver ESP32 is connected to two L298N motor drivers.

- The ESP32 generates control signals for the motor drivers.
- Each L298N motor driver controls two DC motors.
- The motor drivers receive power from an external battery source.
- The four DC motors are connected to the four Mecanum wheels.

Refer to the circuit diagrams included in this repository for the complete hardware connections.

## 🔄 Implementation Procedure

1. Install the ESP32 Board Manager in Arduino IDE.
2. Install the required MPU6050 and I2Cdev libraries.
3. Connect the MPU6050 sensor to the transmitter ESP32.
4. Establish the connections between the receiver ESP32 and motor drivers.
5. Upload the MAC address identification code to obtain the receiver's MAC address.
6. Configure the transmitter and receiver for wireless communication.
7. Upload the transmitter and receiver programs to their respective ESP32 boards.
8. Power the vehicle using the battery source.
9. Control the vehicle by performing different hand gestures.

## 📊 Result

Successfully developed a wireless Hand Gesture Controlled Car using ESP32 microcontrollers and an MPU6050 IMU sensor.

The system detects hand movements, processes the sensor readings, and transmits corresponding control commands wirelessly to the receiver. The receiver controls the four DC motors through motor drivers, enabling the vehicle to move according to the user's hand gestures.

This project demonstrates the practical application of IMU sensors, embedded systems, wireless communication, and motor control in robotics.

## 📚 Libraries and References

- **ESP32 Board Manager:** https://dl.espressif.com/dl/package_esp32_index.json
- **MPU6050 and I2Cdev Library:** https://github.com/jrowberg/i2cdevlib

## 🎥 Project Demo Video
Click below to watch the project demonstration on LinkedIn!

https://www.linkedin.com/posts/gone-ramu-2155092b2_hand-gesture-controlled-car-using-mpu6050-ugcPost-7527345551101784065-8P75/?utm_source=share&utm_medium=member_desktop&rcm=ACoAAEsumfEBdfpbRoL04rRFCpsATJalW3cUVUA

**Note : go through the project report section for more details.**
