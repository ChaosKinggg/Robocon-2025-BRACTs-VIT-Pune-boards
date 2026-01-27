# Pneumatics Solenoid Driver Board RC-25  
**System Integration & Rapid Deployment Interface Board**

This board was designed to simplify and accelerate **pneumatic system deployment and integration** by providing a compact, reliable, and clearly mapped interface for controlling multiple solenoid valves from a microcontroller.  
The board enables clean, fast, and safe actuation of **up to 8 pneumatic solenoids simultaneously**, significantly reducing wiring complexity during robotics development.

<p align="center">
  <img src="./In-House%20Prototype/43729.jpg.jpeg" width="650"><br>
  <em>In-House Prototype of discrete N-MOS H-bridge PMDC motor driver</em>
</p>

---

## Design Files
The following design Files are included in this repository:

- [**Deployed Build**](./Deployed%20Build)
- [**3D View**](./3D)  
- [**PCB Layout**](./Layout)
- [**Schematic**](./Schematic) 

All files are organized into their respective folders for easy navigation. 

---

## Design Objectives
- Enable fast and reliable control of multiple pneumatic solenoids
- Reduce wiring clutter and GPIO management complexity
- Provide clear channel-to-GPIO mapping for quick system integration
- Ensure electrical safety and robustness during solenoid actuation
- Support both manual and MCU-driven control modes

---

## Solenoid Actuation Interfaces
- **8 independent solenoid channels**
- Each channel capable of driving one pneumatic solenoid valve
- All channels can be actuated **simultaneously**
- Designed for use with common DC solenoid valves in robotic systems

---

## Control & Interface Architecture

### GPIO Interface (FRC Connector)
- **Single FRC connector** breaking out control signals for all 8 channels
- Allows connecting all solenoid control lines to MCU GPIOs using one cable
- Clear on-board labeling indicating:
  - Channel number
  - Corresponding GPIO pin for **Arduino Mega**
  - Corresponding GPIO pin for **STM32F407-DISC1**
- Enables fast, error-free wiring during deployment

---

### Dual Control Mode (Manual + GPIO)
Each solenoid channel can be actuated using:
- **MCU GPIO logic**  
- **On-board tactile push button**

This allows:
- Manual testing of solenoids without firmware
- Debugging during bring-up and integration

---

## Protection & Reliability Features
- **Flyback diodes on every channel**
  - Protects MOSFETs and logic circuitry from inductive voltage spikes
  - Eliminates damage caused by solenoid magnetic field collapse
- **GPIO over-voltage protection**
  - Diode protection when channels are actuated using tactile switches
  - Prevents back-feeding or over-voltage on MCU GPIOs
- **MOSFET-based switching**
  - Low heat dissipation
  - Compact and reliable channel implementation

---

## Power Architecture & Control
- **Single XT30 power connector** for solenoid power input
- On-board **power LED** indicating board power status
- **Push-lock power switch** to turn solenoid power ON/OFF

---

## Indicators & User Interface
- **8 individual channel LEDs**
  - Indicates ON/OFF state of each solenoid channel
  - Enables quick visual debugging
- On-board **power LED** for supply indication
- Tactile switches for direct channel actuation
