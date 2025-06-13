# 👨‍💻 Suryaprakash S — Senior Embedded Hardware Design Engineer

![GitHub repo size](https://img.shields.io/github/repo-size/YourGitHubUsername/Portfolio)
[![LinkedIn Badge](https://img.shields.io/badge/LinkedIn-Profile-blue)](https://www.linkedin.com/in/suryaprakash-embedded)
[![Portfolio Projects](https://img.shields.io/badge/Projects-Embedded_Hardware-orange)](#projects)

🔧 6+ years in embedded hardware design across automotive, industrial automation, power electronics, and consumer tech. I specialize in **multi-layer high-speed PCB layout**, **signal & power integrity**, **firmware-hardware integration**, and **certification-ready product design**.

---

## 📘 Technical Overview

| Area                          | Expertise                                                                 |
|-------------------------------|--------------------------------------------------------------------------|
| **PCB Design**                | 2–6 layer PCBs, impedance control, differential routing, DDR interfaces  |
| **High-Speed Interfaces**     | USB 2.0/3.0, Ethernet (RMII), SPI > 10 MHz, CAN-FD, RS-485               |
| **Microcontrollers & SoCs**   | STM32 (F0–F7), Atmel AVR, dsPIC33, MSP430, SAMD51, R5F                   |
| **Power Systems**             | Synchronous Buck, Flyback, MPPT, LDOs, SMPS, BMS                         |
| **Simulation Tools**          | LTSpice, PI Advisor, TINA-TI, HyperLynx (basic), MATLAB Simulink         |
| **Design Tools**              | Altium Designer, EAGLE, Cadence Allegro                                  |
| **Testing Equipment**         | Mixed-signal Oscilloscopes, Logic Analyzers, EMI Pre-scan, Power Analyzer|
| **Standards & Compliance**    | EMI/EMC (CISPR 25, IEC 61000), UL, CE, ISO 7637, IPC-2221               |

---

## 🚀 Project Portfolio

### ⚡ High-Speed EV Charging Controller (AC Level 2)

- **MCU:** STM32F407 | **Layers:** 4 | **Speed:** SPI @ 20 MHz, CAN @ 1 Mbps
- **Features:** Load monitoring, temperature foldback, relay cutoff logic
- **Compliance:** IEC 61851, CISPR 25 EMI tests (pre-scan verified)
- **Highlights:**
  - Designed impedance-controlled CAN and SPI traces (controlled stack-up)
  - Implemented opto-isolated RS-485 and CAN communication
  - Achieved <±5% ripple on 12V rail under dynamic switching load

📂 `EV_Charging_Station/`

---

### 🔋 High Current BMS – 8S Active Balancing

- **Topology:** Synchronous flyback-based balancing @ 4A/channel
- **MCU:** STM32G0 | **Protection:** OVP, UVP, OTP, reverse polarity
- **Firmware:** SOC estimation with Kalman filter + voltage lookup
- **Highlights:**
  - Designed thermal foldback circuit using NTC + comparator + shutdown logic
  - Real-time data logging via UART and CAN with CRC integrity checks
  - Simulation-based validation of inductor ripple and thermal rise

📂 `BMS_Design/`

---

### 🧵 Textile Auto-Winder Controller (Legacy to MCU Conversion)

- **Conversion:** Siemens S7 PLC → STM32F103 + BLDC driver
- **Comm Protocols:** UART, RS-485 Modbus
- **PCB Stack:** 2-layer compact board with isolated supply
- **Highlights:**
  - Achieved 20% cost reduction with faster response time
  - BLDC PID closed-loop speed control with encoder feedback
  - EMI compliant below CISPR class A limit

📂 `Textile_Automation/`

---

### ☀️ Solar MPPT Hybrid Controller

- **MCU:** STM32F030 | **MPPT Algo:** Perturb & Observe
- **Features:** Dual-path power switching (solar + grid), load priority control
- **Protection:** Battery temp, reverse polarity, low-load cutoff
- **Highlights:**
  - Implemented dynamic MPPT switching with debounce and soft start
  - Designed SMPS (flyback) with <2% line regulation under load transients

📂 `Solar_Hybrid_Controllers/`

---

## 📈 System Design Best Practices

- ✅ **High-Speed Routing:** Length-matched SPI/USB, controlled impedance differential pairs
- ✅ **Signal Integrity:** Ground return planning, stitch vias, EMI filters
- ✅ **Power Integrity:** Decoupling cap optimization, ripple analysis, LDO placement
- ✅ **Reliability:** MTBF analysis, worst-case derating, hot-swap protection
- ✅ **Production Ready:** BOM optimization, part lifecycle checks, DFMEA reports

---

## 🧰 Tools Used

```yaml
Design:
  - Altium Designer (HDI, RF & multilayer boards)
  - CadSoft EAGLE (rapid prototyping)
  - Cadence Allegro (for high-speed & constraint-driven layout)
  - KiCad (open-source compatibility)
  - EasyEDA (quick design validation and component libraries)

Simulation:
  - LTSpice (switching regulators, analog front-end)
  - PI Advisor (power integrity analysis)
  - MATLAB Simulink (control algorithms & filter design)
  - TINA-TI (analog & power circuit behavior)
  - HyperLynx (signal/power integrity, basic DDR simulation)
  - Keysight ADS (for RF/high-speed optional extensions)

Firmware IDE:
  - STM32CubeIDE (STM32 development and HAL/LL layer integration)
  - MPLAB X IDE (dsPIC/PIC32 development)
  - Energia (TI LaunchPad prototyping)
  - Atmel Studio (AVR and SAM devices)
  - PlatformIO (multi-framework embedded dev)

Protocols:
  - UART, SPI, I²C, CAN, CAN-FD, LIN, RS-232, RS-485
  - Modbus RTU/ASCII, USB 2.0/3.0 (Device & Host)
  - Ethernet (RMII, TCP/IP stack integration)
  - 1-Wire (sensor and ID devices)
  - SWD/JTAG (debugging & boundary scan)

Standards:
  - CISPR 25, CISPR 11 (EMI/EMC for automotive & industrial)
  - UL 94V-0 (flammability), UL 1998 (software safety)
  - IEC 61000 series (ESD, surge, EFT, immunity)
  - ISO 7637 (vehicle transient protection)
  - IPC-2221, IPC-7351 (PCB layout and footprint standards)
  - RoHS, REACH (environmental compliance)

Compliance:
  - EMI Pre-scan (CISPR-based conducted/radiated tests)
  - Power Cycling Test (relay/latching system validation)
  - Temperature Stress Test (hot/cold ramp soak profiles)
  - Thermal Cycling: −40 °C to +85 °C (IEC 60068-2-14)
  - Vibration Test: IEC 60068-2-6 (sinusoidal vibration profile)
  - Mechanical Shock Test: IEC 60068-2-27
  - ESD Immunity: IEC 61000-4-2 (±8kV air, ±4kV contact)
  - Surge Immunity: IEC 61000-4-5 (1.2/50 µs wave)
  - EFT/Burst Test: IEC 61000-4-4 (transients via power lines)
  - HALT/HASS: Highly Accelerated Life and Stress Screening
  - Burn-in Testing: 72–168 hour at 100% load with thermal soak
  - MTBF Analysis: Reliability prediction (MIL-HDBK-217)
  - DFMEA, PFMEA: Failure mode analysis for design/process validation

