<div align="center">

# Reptide — Smart Gym Tracker

### Embedded IoT System for Real-Time Workout Monitoring

<br>

<img src="media/The%20device.png" width="620">

<br><br>

<p>
  <img src="https://skillicons.dev/icons?i=cpp,arduino,flutter,dart,firebase&perline=5" />
</p>

<p>
  <b>ESP32 · MPU6050 · BLE · Flutter · KiCad · SolidWorks · UML</b>
</p>

</div>

---

## Overview

Reptide is an embedded IoT fitness monitoring system developed as a
final-year engineering project.

The system combines an inertial motion sensor, an ESP32-based embedded
device, Bluetooth Low Energy communication, and a Flutter application to
monitor workout movements and provide real-time performance information.

The project was developed as an end-to-end system rather than as an
isolated software application. It covers the interaction between the
physical sensing layer, embedded processing, wireless communication,
mobile software, data management, and the physical integration of the
electronics.

At the hardware level, the system uses an **ESP32 DevKit WROOM-32** as
the main microcontroller and an **MPU6050** accelerometer and gyroscope
for motion sensing.

The embedded device communicates with the application through
**Bluetooth Low Energy (BLE)**, allowing workout information to be
transmitted to the user interface during operation.

---

## Project Objectives

The main objective of Reptide is to provide a connected system capable of
monitoring strength-training movements and transforming motion data into
useful workout information.

The system was designed around several objectives:

- Acquire movement data from an inertial sensor
- Process motion data using an embedded microcontroller
- Detect and count exercise repetitions
- Measure movement phases and performance-related parameters
- Transmit workout information wirelessly
- Display workout information in real time
- Store workout history
- Provide post-workout performance analysis
- Integrate the electronics into a compact physical device

The project also extends beyond the embedded tracker through a broader
fitness application incorporating workout management and additional
fitness-related tracking functionality.

---

# System Architecture

The Reptide system is organized into several interacting layers:

```text
┌──────────────────────────────────────────────┐
│              PHYSICAL MOVEMENT              │
└──────────────────────┬───────────────────────┘
                       │
                       ▼
┌──────────────────────────────────────────────┐
│                  MPU6050                     │
│       3-Axis Accelerometer + Gyroscope      │
└──────────────────────┬───────────────────────┘
                       │
                       │ I²C
                       ▼
┌──────────────────────────────────────────────┐
│                   ESP32                      │
│       Embedded Processing + BLE Server       │
└──────────────────────┬───────────────────────┘
                       │
                       │ Bluetooth Low Energy
                       ▼
┌──────────────────────────────────────────────┐
│             Flutter Application              │
│      Connection · Workout · Analysis         │
└──────────────────────┬───────────────────────┘
                       │
                       ▼
┌──────────────────────────────────────────────┐
│          User & Performance Data              │
│       History · Statistics · Feedback        │
└──────────────────────────────────────────────┘
