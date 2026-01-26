# ESP32 Server–Client Buffer Board RC-25  
**System Integration & Rapid Prototyping Interface Board**

This buffer board was designed to enable **distributed system deployment and integration** using **two ESP32 DevKit V1 boards**, configured in a **Server–Client architecture**.  
The intent of the board is to separate **wireless control logic** from **real-time sensor acquisition**, while providing clean, robust interfaces to external controllers such as **STM32F407 DISC1** and **Arduino Mega**.

The Server ESP32 handles all wireless operations, while the Client ESP32 is dedicated to sensor data acquisition and wired communication.

---

## 🎯 Design Objectives
- Enable clear separation of wireless control and sensor acquisition
- Reduce system latency by offloading time-critical tasks to a dedicated client
- Provide structured, application-oriented breakouts for sensors and communication
- Enable reliable wired communication to external controllers
- Improve power safety, robustness, and system-level control

---

## 🧠 System Architecture Overview
- **Server ESP32**
  - Handles wireless communication
  - Receives commands from control applications
  - Updates system state and parameters
- **Client ESP32**
  - Dedicated to sensor data acquisition
  - Interfaces with encoders and IMU
  - Forwards acquired data to STM32 / Arduino Mega via UART or RS-485

---

## 🔌 Controller Communication Interfaces
- Wired communication from **Client ESP32** to external controllers
- Designed to interface with:
  - STM32 microcontrollers
  - Arduino Mega
- Communication supported via UART or RS-485 for noise-immunity

---

## 🔄 Encoder Interfaces (Client ESP32)
- **4 dedicated terminal blocks** for optical rotary encoders
- On-board **pull-up resistors** provided for encoder signals
- Designed for direct connection of incremental encoders
- Encoder data acquired exclusively by the Client ESP32

---

## 🔧 Actuation & Expansion Interfaces

### I²C & Sensor Interfaces (Client ESP32)
- **Dedicated I²C terminal block**
- Optional **external I²C pull-up resistors**
- **Dedicated pin headers for BNO055 IMU**
  - Sensor mounted directly onto the buffer board
  - Reduces wiring complexity and improves signal integrity
- Sensor fusion and data acquisition handled by Client ESP32

---

## 🔗 Communication Interfaces

### UART
- **Both Server and Client ESP32 UARTs broken out**
- Each UART having **two alternative terminal blocks**:
  - Standard UART (TX/RX)
  - RS-485 interface

### RS-485 Support
- On-board RS-485 transceivers enabling UART-to-RS485 communication
- Direction control configurable using **0-ohm jumpers** for:
  - Transmit
  - Receive
- Enables robust long-distance, noise-immune communication with external controllers

---

## 🌐 Wireless Control & Reset Capability (Server ESP32)
- Server ESP32 receives commands wirelessly from control applications
- Supports remote control operations including:
  - Resetting **Client ESP32**
  - Resetting connected **STM32**
  - Resetting connected **Arduino Mega**
- Enables centralized system control without physical access

---

## ⚡ Power Architecture & Protection
- **Two XT30 power connectors**
  - XT30 #1: Powers logic, wireless modules, and peripherals **except encoders**
  - XT30 #2: Dedicated power rail for encoders
- Separate power rails to reduce noise coupling
- On-board **voltage regulation** for ESP32 and peripherals
- **Reverse polarity protection** integrated at power input
- **Push-lock power switch** to turn board power ON/OFF

---

## 💡 Indicators & User Interface
- On-board **power LEDs**
- Dedicated **user LEDs**
- Visual feedback for board power, system status, and operation

---

## 📐 Design Files
The following design Files are included in this repository:

- [**Schematic**](./Schematic) 
- [**PCB Layout**](./Layout)
- [**3D View**](./3D)  
- [**In-House Prototype**](./Tn-House%20Prototype)  
- [**Deployed Build**](./Deployed%20Build)

All files are organized into their respective folders for easy navigation. 
