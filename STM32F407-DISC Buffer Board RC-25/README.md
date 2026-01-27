# STM32F407-DISC Buffer Board RC-25 
**System Integration & Rapid Deployment Interface Board**

This extension board was designed to significantly simplify and accelerate **system Deployment and integration** around the **STM32F407 Discovery (DISC1) development board**.  
The goal of the board is to provide clean, organized, and application-oriented breakouts for motors, encoders, communication interfaces, sensors, and power — reducing wiring complexity and integration time during robotics and embedded system development.

---

## Design Objectives
- Reduce wiring overhead during system integration
- Provide application-specific connectors instead of raw GPIO headers
- Enable quick motor, encoder, sensor, and communication interfacing
- Improve robustness, power safety, and usability over direct dev-board wiring

---

## Motor Driver Interfaces
- **4 dedicated terminal blocks (Relimates)** for Cytron motor drivers
- Each motor interface provides:
  - 2 × PWM pins
  - 2 × Digital direction/control pins
- Enables clean, repeatable motor wiring without breadboards or jumper clutter

---

## Encoder Interfaces
- **5 dedicated terminal blocks** for optical rotary encoders
- On-board **pull-up resistors** provided for encoder signals
- Designed for direct connection of incremental encoders

---

## Actuation & Expansion Interfaces

### FRC-Style Connectors
- **2 dedicated FRC terminal blocks**
  - **Analog FRC Connector**
    - Breaks out ADC-capable STM32 pins
    - Intended for connection to external analog breakout boards
    - Simplifies interfacing of analog sensors
  - **Digital FRC Connector**
    - Breaks out digital GPIO pins
    - Designed for driving pneumatic solenoids and other digital actuators

---

## Communication Interfaces

### UART
- **3 STM32 UARTs broken out**
- Each UART having **two alternative terminal blocks**:
  - Standard UART (TX/RX)
  - RS-485 interface

### RS-485 Support
- **3 on-board MAX485 transceivers** enables UART-to-RS485
- RS485 Direction control configurable using **0-ohm jumpers** for:
  - Transmit
  - Receive
- Enables robust long-distance noise-immune communication

---

### USB Virtual COM Port (VCP)
- STM32F407 Discovery lacks native VCP
- A **4th UART** is broken out as an **FTDI interface**
- Allows attaching an external FTDI module
- Enables USB-to-UART debugging and logging

---

## I²C & Sensor Interfaces
- **Dedicated I²C terminal block**
- Option to populate **external I²C pull-up resistors**
- **Dedicated pin headers for BNO055 IMU**
  - Sensor can be mounted directly onto the extension board
  - Reduces wiring and improves mechanical stability

---

## Power Architecture & Protection
- **Two XT30 power connectors**
  - XT30 #1: Powers dev board and all peripherals **except encoders**
  - XT30 #2: Dedicated power rail for encoders
- On-board **3.3 V LDO regulator**
- **Reverse polarity protection** integrated at power input
- **Push-lock power switch** to turn board power ON/OFF
- **External reset button** to reset the STM32 Discovery board

---

## Indicators & User Interface
- On-board **power LEDs**
- Dedicated **user LED**
- Visual feedback for board power and system state

---

## 📐 Design Files
The following design Files are included in this repository:

- [**Deployed Build**](./Deployed%20Build)
- [**In-House Prototype**](./Tn/-House-Prototype)
- [**3D View**](./3D)  
- [**PCB Layout**](./Layout)
- [**Schematic**](./Schematic) 

All files are organized into their respective folders for easy navigation.
