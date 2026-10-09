---
title: Projects
description: Hardware engineering case studies, PCB design, and embedded systems developed by Edgar Vela.
---

# Engineering Projects

Below is a curated selection of engineering projects spanning high-speed multi-layer PCB design, bare-metal & RTOS firmware development, and hands-on laboratory validation.

---

## Project 1: Ultra-Low Power Industrial IoT Sensor Node

!!! info "Project Overview"
    End-to-end design of an autonomous, low-power industrial condition-monitoring node featuring long-range wireless connectivity (LoRaWAN) and local Bluetooth Low Energy (BLE) for field diagnosis and parameterization via a mobile app.

### :material-cogs: Technical Specifications

- **Processing Unit**: STM32L4 Microcontroller (ARM Cortex-M4 @ 80 MHz with FPU).
- **Connectivity**: SX1262 LoRaWAN transceiver (868 MHz / 915 MHz bands) and nRF52832 Bluetooth Low Energy SoC.
- **Integrated Sensors**:
    - Low-noise triaxial accelerometer (SPI interface with internal FIFO for vibration anomaly detection).
    - Environmental sensor measuring temperature, relative humidity, and barometric pressure.
- **Power Architecture**: 3.6 V Li-SOCl2 primary battery with nano-quiescent buck converter (< 1 µA quiescent current).
- **Battery Life Target**: > 5 years autonomous operation with 15-minute transmission intervals.
- **PCB Topology**: 4-layer stackup (FR4 TG150, SIG-GND-PWR-SIG, 50 Ω controlled impedance for the RF trace).

### :material-code-tags: Technical Stack

| Domain | Tools & Technologies |
| :--- | :--- |
| **Hardware Design** | Altium Designer, SPICE power supply simulation, DFM/DFA analysis |
| **Embedded Firmware** | C (C99), STM32CubeIDE, FreeRTOS, Semtech LoRaWAN stack, BLE GAP/GATT services |
| **Validation & Test** | Otii Arc (Power Profiler), Keysight InfiniiVision Oscilloscope, RF Spectrum Analyzer |

### :material-check-decagram: Key Results & Achievements

- **Sleep Current**: Achieved an average quiescent sleep current of **4.2 µA**, exceeding the initial target of 8 µA.
- **RF Performance**: Measured return loss $S_{11} < -18 \text{ dB}$ at 868 MHz following Pi-network impedance tuning.
- **Production Yield**: Successfully manufactured and assembled a pilot batch of 50 units with zero assembly defects (DFT implemented with bed-of-nails test points).

---

## Project 2: High-Efficiency BLDC Motor Controller

!!! info "Project Overview"
    Compact three-phase inverter for driving BLDC and permanent magnet synchronous motors (PMSM) using Field-Oriented Control (FOC), engineered for mobile robotics and high torque-density actuators.

### :material-cogs: Technical Specifications

- **Input Voltage Range**: 18 V to 52 V DC (supporting up to 12S Li-Ion battery packs).
- **Current Rating**: 30 A continuous / 70 A peak with passive thermal dissipation.
- **Power Stage**: Three-phase half-bridge utilizing ultra-low $R_{DS(on)}$ MOSFETs (1.8 mΩ) and isolated gate drivers with hardware shoot-through protection.
- **Current Sensing**: Low-inductance tri-shunt configuration with low-drift bidirectional current sense amplifiers.
- **Communication Interfaces**: Galvanically isolated CAN-FD bus and high-speed UART/USB telemetry port.
- **PWM Frequency**: 20 kHz to 40 kHz with center-aligned PWM and ADC sampling synchronized at the midpoint.
- **PCB Topology**: 6-layer heavy-copper board (2 oz outer, 3 oz inner layers) for thermal conduction and low ESR power routing.

### :material-code-tags: Technical Stack

| Domain | Tools & Technologies |
| :--- | :--- |
| **Hardware Design** | KiCad 8.0, FEA thermal simulation, continuous ground plane design |
| **Control Algorithms** | FOC (Clarke/Park transformations, Space Vector PWM - SVPWM), closed-loop current and velocity PI loops |
| **Firmware Architecture** | Embedded C++ (C++17), CMSIS-DSP, deterministic non-blocking design |
| **Validation Instruments** | Dynamometer test bench, Hall-effect current probes, FLIR thermal imaging |

### :material-check-decagram: Key Results & Achievements

- **Power Efficiency**: Peak inverter efficiency of **96.8%** at rated nominal load.
- **Dynamic Control**: Current control loop executed at **20 kHz** with less than 12 µs calculation latency on the MCU.
- **Fault Protection**: Hardware-level cycle-by-cycle overcurrent trip, bus overvoltage clamping, and over-temperature shutdown.

---

## :material-folder-multiple: Template for New Projects

To document additional projects in this portfolio, use the following standardized structure:

```markdown
## Project Name

!!! info "Project Overview"
    High-level summary of the engineering objectives and product value.

### :material-cogs: Technical Specifications
- **Parameter 1**: Description.
- **Parameter 2**: Description.

### :material-code-tags: Technical Stack
| Domain | Tools & Technologies |
| :--- | :--- |
| Hardware | ECAD software, simulations, layout standards |
| Firmware | Languages, RTOS, driver libraries |

### :material-check-decagram: Key Results & Achievements
- Quantifiable metrics verified during lab validation.
```
