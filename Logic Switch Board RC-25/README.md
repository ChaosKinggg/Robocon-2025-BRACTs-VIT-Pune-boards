# Logic Switch Board RC-25  
**System Integration & Low-Power Distribution Interface Board**

This board was designed as a **relay-based logic power distribution board** for robotics and it is intended to safely distribute **12 V power to logic circuits**.

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
- Safely distribute logic supply power across multiple subsystems
- Enable emergency shutdown via an external kill switch

---

## Power Distribution Interfaces
- **6 XT30 connectors** for logic power distribution
- Designed to distribute **12 V logic supply** to multiple downstream boards
- Allows centralized power routing instead of multiple battery splitters

---

## Switching Architecture
- **Relay-based power switching**
- Relay used to isolate and control logic power distribution
- Suitable for handling higher currents compared to direct electronic switching
- Switching is **manual only** and requires user interaction

---

## Control & Actuation Interfaces

### Power Enable Options
Two independent methods provided to turn ON the logic power rail:

- **Push-lock switch**
  - Direct on-board manual control
  - Requires deliberate press to change power state
- **External kill switch (Relimate connector)**
  - Designed to connect to an externally mounted, easily accessible kill switch
  - Intended for emergency shutdown in out-of-control situations

### Selection Mechanism
- Power enable source selected using **shorting selection flags**
- Allows choosing between:
  - On-board push-lock switch
  - External kill switch input

---

## Protection & Safety Features
- **Flyback diode across relay coil**
  - Protects circuitry from inductive voltage spikes
  - Improves relay reliability and longevity
- Designed for fail-safe behavior during system faults

---

## Power Status Indication
- **Battery presence LED**
  - Indicates that the power source is connected
- **Logic power ON LED**
  - Indicates that the logic distribution rail is active
- Clear visual separation between supply availability and switched output
