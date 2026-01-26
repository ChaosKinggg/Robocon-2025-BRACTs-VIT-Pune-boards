# Power Switch Board RC-25  
**System Integration & High-Power Distribution Interface Board**

This board was designed as a **relay-based main power distribution board** for robotics operating at **24 V**.
It is intended to safely distribute **high-power supply voltage** to downstream Power electronics systems.

This board can be used **in parallel with the Logic Switch Board**, where a buck converter steps down **24 V → 12 V** to power logic electronics.

---

## 🎯 Design Objectives
- Safely distribute high-power supply voltage across multiple subsystems
- Provide a clear and reliable manual power control mechanism
- Enable emergency shutdown via an external kill switch
- Improve system safety during testing and deployment
- Allow clean separation of power and logic domains
- Prevent damage to downstream systems during power switching

---

## 🔌 Power Distribution Interfaces
- **XT60 connectors** for power output distribution
- Designed to operate at **24 V**
- Suitable for higher current delivery compared to logic-level distribution
- Enables centralized power routing to motor drivers, converters, and power-hungry peripherals

---

## 🔄 Switching Architecture
- **Relay-based power switching**
- Relay used to isolate and control the main power rail
- Designed to handle higher voltage and current levels
- Switching is **manual only** and requires deliberate user interaction

---

## 🔧 Control & Actuation Interfaces

### Power Enable Options
Two independent methods provided to turn ON the main power rail:

- **Push-lock switch**
  - Direct on-board manual control
  - Requires intentional press to change power state
- **External kill switch (Relimate connector)**
  - Designed to connect to an externally mounted, easily accessible kill switch
  - Intended for emergency shutdown in out-of-control situations

### Selection Mechanism
- Power enable source selected using **shorting selection flags**
- Allows choosing between:
  - On-board push-lock switch
  - External kill switch input

---

## 🛡 Protection & Safety Features
- **Flyback diode across relay coil**
  - Protects control circuitry from inductive voltage spikes
  - Improves relay reliability and operational lifetime
- Manual switching prevents unintended or software-induced power cycling
- Designed for fail-safe behavior during system faults

---

## ⚡ Power Status Indication
- **Battery presence LED**
  - Indicates that the 24 V supply is connected
- **Main power ON LED**
  - Indicates that the switched power rail is active
- Clear distinction between supply availability and enabled output

---

## 💡 Indicators & User Interface
- Two on-board **power LEDs** for system status visibility
- Push-lock switch for direct operator control
- External kill switch interface for safety-critical remote access

---

## 📐 Design Files
The following design Files are included in this repository:

- [**Schematic**](./Schematic)  
- [**PCB Layout**](./Layout)  
- [**3D View**](./3D)  
- [**Deployed Build**](./Deployed%20Build)

All files are organized into their respective folders for easy navigation.
