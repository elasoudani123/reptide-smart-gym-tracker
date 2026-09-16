<div align="center">

# 🏋️ Reptide — Smart Gym Tracker

### Intelligent Embedded Fitness Monitoring System

<p>
  <b>ESP32 · MPU6050 · BLE · Flutter · PCB Design · 3D Enclosure</b>
</p>

<br>

<img src="media/The%20device.png" width="650">

<br><br>

<p>
  <i>
    A connected embedded system designed to monitor movement,
    track exercise performance and provide real-time feedback.
  </i>
</p>

</div>

---

# 🧠 About Reptide

**Reptide** is an intelligent fitness monitoring system that combines
embedded hardware, motion sensing, wireless communication and a mobile
application to provide real-time workout monitoring and performance analysis.

The system is designed around an **ESP32 microcontroller** and an
**MPU6050 inertial measurement unit**, with communication between the
embedded device and the application performed through **Bluetooth Low Energy
(BLE)**.

The project combines:

- ⚙️ Embedded systems
- 📐 Motion sensing
- 📡 Bluetooth Low Energy
- 📱 Mobile application development
- 🔌 PCB design
- 📦 3D enclosure design
- 📊 Real-time monitoring
- 🧠 Intelligent workout analysis

---

# 🎯 Project Objectives

The main objective of Reptide is to develop an accessible system capable of
monitoring and analyzing strength-training movements while providing useful
feedback to the user.

The system was designed to:

- 🔢 Detect and count exercise repetitions
- 📈 Analyze movement performance
- ⚡ Provide real-time workout information
- 📊 Track performance metrics
- 📝 Store workout history
- 💡 Provide feedback based on movement performance
- 📱 Connect the embedded device to a mobile application

The broader application also incorporates fitness-related tracking features
such as nutrition and sleep monitoring.

---

# 🏗️ System Architecture

The overall Reptide system connects the physical sensing layer to the
mobile application through an embedded processing and wireless communication
layer.

<p align="center">
  <img src="docs/project-block-diagram.png" width="850">
</p>

### System Flow

```text
             PHYSICAL MOVEMENT
                    │
                    ▼
             ┌─────────────┐
             │   MPU6050   │
             │ Accelerometer│
             │ + Gyroscope │
             └──────┬──────┘
                    │
                    ▼
             ┌─────────────┐
             │    ESP32    │
             │ Embedded    │
             │ Processing  │
             └──────┬──────┘
                    │
                    │ BLE
                    ▼
             ┌─────────────┐
             │   Flutter   │
             │ Application │
             └──────┬──────┘
                    │
                    ▼
             ┌─────────────┐
             │ Workout &   │
             │ Performance │
             │ Monitoring  │
             └─────────────┘
