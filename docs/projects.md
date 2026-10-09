---
title: Projects
description: Engineering and research projects developed by Edgar Marcelo Vela Pinela across biomedical devices, DSP, and embedded systems.
---

# Engineering & Research Projects

A showcase of real-world hardware, embedded systems, and scientific research projects developed across Swiss research institutes, high-tech industry, and university laboratories.

---

## Project 1: Point-of-Care Polymerase Chain Reaction (PCR) Devices

!!! info "Project Context — ETH Zürich & DIAXXO AG (Dec 2020 — Present)"
    Full-lifecycle hardware and software development for next-generation, rapid Point-of-Care PCR diagnostic instruments, transitioning advanced biotechnology from laboratory prototypes to certified commercial devices.

### :material-cogs: Engineering Scope & Contributions

- **Electronic Hardware Design**:
    - Complete schematic design and multi-layer PCB layout using **Altium Designer** for ultra-fast thermal cycling, optical fluorescence measurement, and power management.
    - Precision analog signal acquisition circuitry for optical biosensors with high signal-to-noise ratio (SNR).
    - Design for electromagnetic compatibility (EMC/EMI) and low-noise operational conditions.
- **Mechanical & Packaging CAD**:
    - CAD design for rapid prototyping (3D printing, CNC machining) through to injection-molding production housings.
    - Thermal management integration and mechanical tolerance verification.
- **Regulatory, Procurement & Quality Control**:
    - Component selection and strategic procurement complying with global supply chain availability and medical device standards.
    - Authorship of comprehensive manufacturing work instructions and formal Quality Control (QC) verification protocols.
- **Validation & Testing**:
    - Testbench setup for automated board bring-up, sensor calibration, thermal profiling, and biological assay repeatability.

### :material-code-tags: Technical Stack

| Domain | Tools & Technologies |
| :--- | :--- |
| **Electronics CAD** | Altium Designer, SPICE modeling, Multi-layer PCB design |
| **Mechanical Design** | Mechanical CAD modeling, rapid 3D prototyping, thermal integration |
| **Embedded & Software** | Embedded C/C++, test scripting, sensor acquisition algorithms |
| **Compliance & QC** | Regulatory component sourcing, QC protocols, standard work instructions |

---

## Project 2: Audio-Domain DSP using Antenna Arrays and Beamforming

!!! info "Project Context — Institute for Systems and Applied Electronics (SUPSI, 2018 — 2020)"
    Applied scientific research focused on digital signal processing in the audio domain, deploying spatial filtering and acoustic antenna array beamforming algorithms for directional sound capture and noise cancellation.

### :material-cogs: Engineering Scope & Contributions

- **Acoustic Array Architecture**:
    - Spatial sensor placement and multi-channel microphone array integration.
    - Microelectronics and digital signal interface design for simultaneous high-fidelity acoustic sampling.
- **Digital Signal Processing (DSP)**:
    - Implementation of adaptive beamforming algorithms (delay-and-sum, minimum variance distortionless response - MVDR).
    - Spatial filtering, noise suppression, and directional sound localization in reverberant indoor environments.
- **Simulation & Verification**:
    - Extensive algorithm simulation and performance analysis in **MATLAB** and **Simulink** before embedded target deployment.

### :material-code-tags: Technical Stack

| Domain | Tools & Technologies |
| :--- | :--- |
| **Signal Processing** | MATLAB, Simulink, Octave, Beamforming algorithms, Spatial filtering |
| **Hardware & Electronics** | Digital audio interfaces, microphone array electronics, microelectronics |
| **Scientific Discipline** | Digital Electronics, Microelectronics, Bioelectronics |

---

## Project 3: Myoelectric (EMG) Signal Acquisition & FPGA Processing

!!! info "Project Context — ESPOL & IEEE Publications (2016 — 2018)"
    Design and characterization of open-source biomedical hardware for electromyographic (EMG) signal acquisition, thermal influence modeling, and real-time sensor calibration using embedded FPGA processors.

### :material-cogs: Engineering Scope & Contributions

- **Bioelectronics Hardware Design**:
    - Multi-stage biopotential analog front-end (AFE) with instrumentation amplifiers, high CMRR (> 100 dB), active bandpass filtering (20 Hz - 500 Hz), and baseline wander suppression.
    - Schematic design and PCB fabrication for non-invasive surface EMG signal acquisition.
- **FPGA Embedded Implementation**:
    - Implementation of standard gradient descent algorithms on an embedded processor within **Intel/Altera Quartus II** for two-dimensional field sensor calibration.
    - Real-time implementation of a **Dual Extended Kalman Filter (EKF)** for high-precision tilt and state estimation.
- **Biomedical Research & Peer-Reviewed Publications**:
    - Experimental studies on the influence of ambient and muscle temperature variations on EMG spectral and onset characteristics, resulting in multiple IEEE and indexed journal publications.

### :material-code-tags: Technical Stack

| Domain | Tools & Technologies |
| :--- | :--- |
| **EDA & FPGA** | Intel/Altera Quartus II, OrCAD-PSpice, Eagle, Proteus |
| **Analysis & Algorithms** | MATLAB, Simulink, Dual Extended Kalman Filter, Gradient Descent |
| **Microcontrollers** | STM32, PIC (MikroC Pro), Arduino |
| **Academic Output** | 8+ published research papers and 2 Certificates of Merit |
