# Gun Control Box (GCB)

##  Objective
The Gun Control Box (GCB) project involved designing and developing a **real-time embedded control system** for the **main battle tank’s gun stabilization and motion control**.  
The system’s objective was to precisely control the **azimuth and elevation** axes of the gun barrel under different operational modes — including **basic aiming** and **image-stabilized modes** — ensuring accurate target tracking and firing stability even in dynamic field conditions.

---

##  Project Overview
The GCB serves as the **core control unit** between the Fire Control Computer (FCS) and the tank’s actuation subsystems.  
It processes **sensor data**, executes **PID-based control algorithms**, and generates **motor drive commands** to achieve stable and responsive motion control.  

The control loop operates deterministically with a **timing cycle**, maintaining closed-loop synchronization between command input, feedback sensors, and motor output.

---

##  Skills Demonstrated
- Real-time **embedded firmware design** using STM32F4 microcontroller.  
- Development and tuning of **cascaded PID controllers** for azimuth and elevation stabilization.  
- Implementation of **sensor fusion** using gyro and position feedback for accurate angular control.  
- Integration of **CAN Bus**, **SPI**, and **I2C** communication interfaces for subsystem coordination.  
- Experience in **low-level debugging** using ST-Link, oscilloscopes, and CAN bus sniffers.  
- Design of **fault-safe control logic** for mission-critical embedded systems.  

---

##  Tools & Technologies Used
| Category | Tools / Technologies |
|-----------|----------------------|
| **Microcontroller** | STM32F407 (ARM Cortex-M4) |
| **Programming Language** | Embedded C |
| **Control Algorithm** | Cascaded PID Controller (Inner Rate + Outer Position loop) |
| **Communication Interfaces** | CAN, SPI, I2C, UART |
| **Development Tools** | STM32CubeIDE, Keil uVision, Logic Analyzer, ST-Link |
| **Testing Equipment** | Oscilloscope, CAN Analyzer |
| **Hardware Design** | Altium Designer for control board schematics and layout |


---

##  Implementation Summary
- Implemented **real-time closed-loop control** at 420 µs timing interval.  
- Designed **dual control modes**:
  - *Manual aiming mode* (joystick input to motor control)
  - *Image-stabilized mode* (gyro feedback compensation)
- Developed **firmware modules** for:
  - Drive computation and scaling
  - Gyro filtering and rate integration (θ calculation)
  - CAN message parsing and response
  - Overcurrent and safety limit handling

---

##  Results & Testing
- Achieved **smooth and stable motion** with steady-state error under **5%** during field testing.  
- Verified **loop timing consistency** using logic analyzer traces.  
- Successfully integrated the system with the Fire Control Computer (FCS) for full firing sequence validation.  
- Demonstrated operational reliability during **tank vibration and rough terrain trials**.

---


##  Contact
**Muhammad Huzaifa**  
Embedded Systems Designer | Islamabad, Pakistan  
📧 [huzaifazahid888@gmail.com](mailto:huzaifazahid888@gmail.com)  
🔗 [linkedin.com/in/huzaifa-engineer](https://linkedin.com/in/huzaifa-engineer)


