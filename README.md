## 📌 About the Project
This project was developed to provide a highly efficient motor driving experience for electric vehicles. Designed within the [Team Name] team, this hardware is built on a 4-layer PCB architecture to ensure stable operation under high current and voltage.

### Key Features
* **Operating Voltage:** 72V (Nominal) / 100.8V (Maximum)
* **Power Capacity:** 2.5 kW
* **Motor Type:** Brushless DC (BLDC) Hub Motor
* **Driving Algorithm:** FOC (Field Oriented Control)
* **PCB Structure:** 4-Layer

---

## 🛠️ Hardware Used (BOM Summary)

The table below lists the core components used in the power and control stages of the project:

| Hardware Unit | Component Code / Model | Specifications / Values | Role in Project |
| :--- | :--- | :--- | :--- |
| **Microcontroller (MCU)** | `STM32G474C8T6` | 170MHz, High-Resolution Timer | Executing the driving algorithm and signal generation. |
| **Gate Driver** | `IRS21867` | 600V, High/Low Side | Driving the MOSFETs using PWM signals from the MCU. |
| **Power MOSFETs** | `IPT067N20NM6ATMA1` | 200V, 137A, Low RDS(on) | Switching the high current supplied to the motor. |
| **Current Sensors** | `INA240A1` | Bidirectional, Max. 83A, Enhanced PWM Rejection | Reading phase currents to provide closed-loop control. |
| **Voltage Regulator (Buck)** | `TPS563201` | 12V -> 3.3V, Synchronous Buck | Generating the necessary 3.3V voltage for logic circuits and the MCU. |

*(For the full BOM list, you can check the `Hardware/BOM.csv` file.)*

---

## 📂 Folder Structure
```text
📦 Project-Folder
 ┣ 📂 Hardware
 ┃ ┣ 📜 Schematic.pdf
 ┃ ┣ 📜 PCB_Layout.pdf
 ┃ ┣ 📂 3D
 ┃ ┗ 📜 BOM.csv
