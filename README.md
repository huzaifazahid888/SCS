# **Stabilization Control System (SCS)**

##  Objective
The Stabilization Control System (SCS) project involved designing and developing a **real-time embedded control system** for **multi-axis stabilization**.  
The system’s objective was to precisely control the **azimuth and elevation** axes under different operational modes — including **basic positioning** and **stabilized tracking modes** — ensuring accurate targeting and stability even in dynamic operating conditions.

---

##  Project Overview
The SCS serves as the **core control unit** between the Trajectory Control Computer (TCC) and the actuation subsystems.  
It processes **sensor data**, executes **PID-based control algorithms**, and generates **motor drive commands** to achieve stable and responsive motion control.  

The control loop operates deterministically, maintaining closed-loop synchronization between command input, feedback sensors, and motor output.

---

##  Skills Demonstrated
- Real-time **embedded firmware design** using STM32 microcontroller.  
- Development and tuning of **cascaded PID controllers** for azimuth and elevation stabilization.  
- Implementation of **sensor fusion** using gyro and encoder feedback for accurate angular control.  
- Integration of **CAN Bus**, **SPI**, and **I2C** communication interfaces for subsystem coordination.  
- Experience in **low-level debugging** using ST-Link, oscilloscopes, and CAN bus sniffers.  
- Design of **fault-safe control logic** for mission-critical embedded systems.  

---

##  Tools & Technologies Used
| Category | Tools / Technologies |
|-----------|----------------------|
| **Microcontroller** | STM32 (ARM Cortex-M4) |
| **Programming Language** | C++ |
| **Control Algorithm** | Cascaded PID Controller |
| **Communication Interfaces** | CAN, SPI, I2C |
| **Development Tools** | STM32CubeIDE, Logic Analyzer, ST-Link |
| **Testing Equipment** | Oscilloscope, CAN Analyzer |

---

##  Implementation Summary
- Implemented **real-time closed-loop control** at fix timing interval.  
- Designed **control modes** for stabilized operation using gyro feedback compensation
- Developed **firmware modules** for:
  - Drive computation and scaling
  - Gyro filtering and data fusion
  - CAN message parsing and response
  - Safety limit handling

---

##  Results & Testing
- Achieved **smooth and stable motion** with steady-state error under **5%** during testing.  
- Verified **loop timing consistency** using logic analyzer traces.  
- Successfully integrated the system with the Trajectory Control Computer (TCC).  
- Demonstrated operational reliability during **vibration and rough terrain trials**.


