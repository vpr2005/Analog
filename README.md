# EE301 Analog Circuits Project

**Author:** Vekariya Pritkumar  
**Roll No:** 2023EEB1252  
**Course:** EE301 - Analog Circuits  
**Date:** October 30, 2025  

## Overview
This repository contains all the files, reports, and simulation data for the EE301 Analog Circuits Course Project.  
The project focuses on understanding and simulating fundamental analog circuits using Cadence Virtuoso in 180nm CMOS technology.  

**Topics Covered:**
1. Instrumentation Amplifier (INA)
2. Op-Amp Based Band-Pass Filter (BPF)
3. MOSFET Characterization (NMOS and PMOS)
4. CMOS Inverter Simulation

---

## 1. Instrumentation Amplifier (INA)

### Objective
To derive, simulate, and analyze the differential and common-mode gains of a three-op-amp instrumentation amplifier (INA).

### Key Equations
**Differential Gain:**  
\( A_{v,dm} = \frac{R_5}{R_3} (1 + 2\frac{R_1}{R_g}) \)

**Common-Mode Rejection Ratio (CMRR):**  
\( CMRR_{dB} = 20 \log_{10} (\frac{A_{v,dm}}{A_{v,cm}}) \)

### Results
| Parameter | Value |
|------------|--------|
| Theoretical Av,dm | 8.18 (18.26 dB) |
| Measured Av,dm | 8.126 (18.20 dB) |
| Measured Av,cm | 0.071 (-22.98 dB) |
| CMRR | 41.2 dB |

The amplifier effectively rejects common-mode signals, confirming proper differential operation.

---

## 2. Op-Amp Based Band-Pass Filter (BPF)

### Objective
To design and simulate an active band-pass filter using Op-Amps and study the effect of the quality factor (Q) on selectivity.

### Observations
| Q | Center Frequency (kHz) | Max Gain (dB) | Remarks |
|---|------------------------|---------------|----------|
| 10 | 15.85 | 19.7 | High selectivity, narrow passband |
| 2  | 15.85 | 5.95 | Broader passband, lower gain |

The results confirm the expected relationship between Q and filter selectivity.

---

## 3. MOSFET Characterization (180nm CMOS)

### NMOS and PMOS Studies
Both transistors were simulated with **W/L = 10 µm / 1 µm**.

- **Output characteristics:** ID vs VDS (for NMOS) and ID vs VSD (for PMOS).  
- **Transconductance:** gm vs ID, confirming √ID dependency in strong inversion.  
- **Diode-connected configuration:** Verified diode-like conduction behavior.

These plots and observations demonstrate proper device behavior consistent with theoretical MOSFET models.

---

## 4. CMOS Inverter Simulation

### Objective
To study voltage transfer characteristics (VTC) and transient response of a CMOS inverter.

### Results
- **DC Sweep:** Shows the typical S-shaped VTC with switching threshold near VDD/2.  
- **Transient Simulation:** Input square wave produces inverted output with minor delay and finite rise/fall times.  

These confirm proper inverter operation and switching behavior in CMOS logic design.

---

## Repository Structure
```
EE301_Analog_Circuits_Project/
├── README.md
├── report/
│   └── 2023EEB1252.pdf
├── data/
│   └── (simulation data and Cadence project files)
├── LICENSE
└── .gitignore
```

---

## Tools Used
- **Cadence Virtuoso** (180nm CMOS)
- **LTSpice** / **MATLAB** (for analysis and verification)
- **Report** prepared in LaTeX and compiled to PDF.

---

## License
This project is for educational use only. Redistribution or modification should include credit to the original author.

---

## Acknowledgment
This project was completed as part of EE301 Analog Circuits under the guidance of the course instructor.

---

> For detailed circuit schematics, plots, and numerical analysis, refer to `report/2023EEB1252.pdf`.
