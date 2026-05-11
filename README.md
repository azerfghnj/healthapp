# Asclepius

## Overview

Asclepius is an embedded and IoT-based medical monitoring solution designed for elderly care and patient safety. The project combines real-time physiological monitoring, motion analysis, and wireless communication to detect falls, monitor vital signs, and provide continuous health tracking.

The system is built around the STM32F407VGT6 microcontroller using FreeRTOS for task management and integrates multiple biomedical and environmental sensors.

---

# Project Objectives

* Monitor heart rate and SpO2 in real time
* Measure body temperature continuously
* Detect movement and falls using an accelerometer
* Transmit sensor data wirelessly using ESP8266
* Use multitasking with FreeRTOS for efficient sensor management
* Create a scalable healthcare monitoring platform for elderly assistance

---

# Features

## Real-Time Vital Monitoring

* Heart Rate Monitoring
* Blood Oxygen Saturation (SpO2)
* Body Temperature Measurement

## Fall Detection System

* Motion tracking using accelerometer data
* Fall detection algorithm based on acceleration thresholds
* Real-time alert capability

## Embedded System Architecture

* STM32F407VGT6 Microcontroller
* FreeRTOS multitasking environment
* DMA-based data transfer
* USART communication
* Interrupt-driven events

## Wireless Communication

* ESP8266 Wi-Fi module integration
* Real-time data transmission
* IoT-ready architecture

---

# Hardware Components

| Component                     | Description                                 |
| ----------------------------- | ------------------------------------------- |
| STM32F407VGT6 Discovery Board | Main microcontroller                        |
| MAX30102                      | Heart rate and SpO2 sensor                  |
| MLX90614                      | Infrared temperature sensor                 |
| LIS3DSH                       | Accelerometer for motion and fall detection |
| ESP8266                       | Wi-Fi communication module                  |
| LEDs & Push Buttons           | Debugging and control                       |

---

# Software & Tools

| Tool                   | Purpose                       |
| ---------------------- | ----------------------------- |
| STM32CubeIDE           | Embedded firmware development |
| STM32CubeMX            | Peripheral configuration      |
| FreeRTOS               | Real-time operating system    |
| C Programming Language | Embedded software development |
| UART / USART           | Communication protocol        |
| DMA                    | Efficient data transfer       |
| Git & GitHub           | Version control               |

---

# System Architecture

```text
+-------------------+
|   Sensors Layer   |
|-------------------|
| MAX30102          |
| MLX90614          |
| LIS3DSH           |
+---------+---------+
          |
          v
+-------------------+
| STM32F407VGT6 MCU |
|-------------------|
| FreeRTOS Tasks    |
| DMA Management    |
| UART Communication|
+---------+---------+
          |
          v
+-------------------+
|     ESP8266       |
|  Wi-Fi Module     |
+---------+---------+
          |
          v
+-------------------+
| Monitoring System |
| Mobile App / IoT  |
+-------------------+
```

---

# FreeRTOS Task Priority

| Task          | Priority |
| ------------- | -------- |
| MAX30102 Task | High     |
| LIS3DSH Task  | Medium   |
| MLX90614 Task | Low      |

---

# Communication Flow

1. Sensors collect physiological and motion data.
2. STM32 processes the sensor values.
3. FreeRTOS schedules tasks according to priority.
4. DMA transfers data efficiently.
5. USART sends processed data to ESP8266.
6. ESP8266 transmits data wirelessly.
7. Monitoring platform receives and displays data.

# Android Application

The current repository contains the Android application developed for the Asclepius monitoring platform.

The mobile application was designed to:

* Display physiological data in real time
* Monitor patient status remotely
* Synchronize health data using Firebase
* Provide a user-friendly healthcare monitoring interface
* Support future IoT integration with the embedded system

Technologies used:

* Android Studio
* Java
* Firebase Realtime Database
* Bluetooth / IoT Communication

---

# Installation & Setup

## Requirements

* STM32CubeIDE
* STM32CubeMX
* STM32F4 Discovery Board
* USB ST-Link Driver
* Android Studio
* Pycharm

## Steps

1. Clone the repository:

```bash
git clone https://github.com/azerfghnj/healthapp.git
```

2. Open the Android project using Android Studio.

3. Sync Gradle dependencies.

4. Build and run the application on an Android device or emulator.

5. Configure Firebase if required.

6. Launch the application.

---

# Future Improvements

* Mobile application integration
* Cloud database connectivity
* AI-based health analysis
* GPS emergency tracking
* SMS/Email alert system
* Battery optimization
* Web dashboard for caregivers

# Learning Outcomes

Through this project, the following skills were strengthened:

* Embedded systems development
* STM32 microcontroller programming
* Real-time operating systems (FreeRTOS)
* Sensor integration
* IoT communication systems
* DMA and UART communication
* Software architecture design
* Debugging and optimization

---

# Project Status

Current Status: Completed Academic Prototype

The system has been successfully designed, implemented, tested, and presented as an End-of-Studies Project in Mechatronics Engineering.

---

# Developer

Developed entirely as a solo End-of-Studies Project in Mechatronics Engineering.

## Author

* Mohamed Firas Bekir

## Responsibilities

* Embedded system architecture design
* STM32 firmware development
* FreeRTOS task management
* Sensor integration and calibration
* Fall detection implementation
* Wireless communication setup
* Mobile application development
* Firebase integration
* System testing and debugging
* Technical documentation and presentation

---

# License

This project is developed for educational and research purposes.

---

# Contact

## Mohamed Firas Bekir

* GitHub: [https://github.com/azerfghnj](https://github.com/azerfghnj)
* Repository: [https://github.com/azerfghnj/healthapp](https://github.com/azerfghnj/healthapp)
* Email: [bekirfiras2@gmail.com](mailto:bekirfiras2@gmail.com)

---

# Keywords

STM32, FreeRTOS, Embedded Systems, IoT, Healthcare Monitoring, Elderly Care, ESP8266, MAX30102, MLX90614, LIS3DSH, Mechatronics, Fall Detection, Biomedical Monitoring
