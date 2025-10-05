# Analog Circuits Simulation and Characterization (EE 301 Course Project)

## Overview

This repository contains the results and analysis from a comprehensive analog circuits course project. The objective was to simulate, analyze, and characterize fundamental analog building blocks using Cadence Virtuoso in a 180 nm CMOS technology node.

The project focuses on four main areas:

1. High-performance differential amplification
2. Frequency filtering
3. Semiconductor device characterization
4. Basic digital logic (CMOS inverter)

## Technology and Tools

* **EDA Tool:** Cadence Virtuoso
* **Technology Node:** 180 nm CMOS
* **Simulation Types:** DC Sweep, Transient Analysis, AC Analysis
* **Documentation:** Includes detailed derivations and comparison of theoretical vs. simulated results

## Project Components

### 1. Instrumentation Amplifier (INA) Analysis

* **Configuration:** Three Op-Amp INA
* **Key Findings:**

  * Differential Mode Gain (Av,dm) ≈ 8.126 (≈18.2 dB), 0.7% deviation from theoretical 8.18
  * Common-Mode Rejection Ratio (CMRR) ≈ 114.4 (≈41.2 dB) with intentional resistor mismatch
* **Observation:** Demonstrates strong differential amplification while effectively rejecting common-mode noise, even with component mismatches

### 2. Op-Amp Based Band-Pass Filter (BPF)

* **Theoretical Center Frequency (f₀):** R = 10 kΩ, C = 1 nF → f₀ ≈ 15.92 kHz
* **High Q Case (Q = 10, Rf = 100 kΩ):**

  * AC Analysis f₀ ≈ 15.85 kHz
  * Peak Gain ≈ 19.73 dB
  * Narrow pass-band with high selectivity
* **Low Q Case (Q = 2, Rf = 20 kΩ):**

  * AC Analysis f₀ ≈ 15.85 kHz
  * Peak Gain ≈ 5.96 dB
  * Broader pass-band, lower gain
* **Observation:** Confirms the impact of quality factor Q on filter selectivity

### 3. MOSFET Characterization (180 nm CMOS)

* **Devices:** NMOS and PMOS (W/L = 10 μm / 1 μm)
* **Characterization Performed:**

  | Device          | Measurement                        | Observation                                                                         |
  | --------------- | ---------------------------------- | ----------------------------------------------------------------------------------- |
  | NMOS/PMOS       | Output Characteristics (ID vs VDS) | Shows Triode and Saturation regions; saturation current increases with gate voltage |
  | NMOS/PMOS       | Transconductance (gm vs ID)        | gm increases with ID, following square-root dependence in strong inversion          |
  | Diode-Connected | ID vs VDS                          | Confirms two-terminal behavior; current flows only when V ≥ threshold               |

### 4. CMOS Inverter Simulation

* **Configuration:** MN: W/L = 2 μm/1 μm, MP: W/L = 5 μm/1 μm, Load CL = 100 fF
* **Simulation Results:**

  * **DC Sweep (VTC):** S-shaped transfer characteristic, steep transition, excellent noise margins, full rail-to-rail swing (0 V to 1.8 V)
  * **Transient Analysis:** Applied 10 kHz square wave input, output shows inverted waveform with expected rise/fall times and propagation delay
