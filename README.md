 # Audio Amplifier Design

This project presents the design, simulation and hardware implementation for a multistage analog audio amplifier designed to amplify low-level microphone signals to a level capable of driving a speaker load.

## Overview

This project implements a complete analog audio amplification chain consisting of:

- Microphone Circuit
- Differential Pre-Amplifier
- Common Emitter Gain Stage
- Active Bandpass Filter
- Class AB Power Amplifier
- Speaker Output

The amplifier was designed and tested in both LTSpice simulation and hardware.

---

## Specifications

| Parameter | Value |
|---|---|
| Input Voltage | 10–20 mV peak-to-peak |
| Frequency Range | 20 Hz – 20 kHz |
| Target Voltage Gain | ≈ 500 |
| Output Power | ≈ 1.5 W |
| Load Impedance | ≈ 10 Ω |

---

# Circuit Stages

## 1. Differential Pre-Amplifier

A BJT differential amplifier is used as the pre-amplifier stage.

### Purpose
- Initial amplification
- Noise reduction
- Common-mode signal rejection

### Performance
- Differential Gain ≈ 21.5
- CMRR ≈ 19.53 dB
- High input impedance
- Low output impedance

---

## 2. Common Emitter Gain Stage

The CE amplifier provides most of the voltage amplification.

### Features
- Gain designed around 25
- Biasing optimized for active region operation
- Gain adjusted to compensate for loading effects

### Final Values
- RC = 7.2 kΩ
- RE = 270 Ω

---

## 3. Active Bandpass Filter

An active bandpass filter restricts the signal to the audible frequency range.

### Characteristics
- Lower cutoff ≈ 9.5 Hz
- Upper cutoff ≈ 38.4 kHz
- Unity midband gain

### Purpose
- Remove low-frequency noise
- Remove high-frequency interference
- Preserve audio quality

---

## 4. Class AB Power Amplifier

A Class AB push-pull amplifier drives the speaker load.

### Components Used
- TIP31C
- TIP32C

### Features
- Reduced crossover distortion
- Improved efficiency
- Diode biasing for smooth switching

### Output Power
≈ 1 W into a 10 Ω load

---

# Results

| Metric | Value |
|---|---|
| Simulated Gain | 430.5 |
| Hardware Gain | 410 |
| Slew Rate | 0.546 V/µs |

The amplifier was verified using:
- LTSpice simulations
- Oscilloscope measurements
- Hardware testing

---

# Tools Used

- LTSpice
- Oscilloscope
- Function Generator

---

# Authors

- Gauri Krishnan
- Sukeerthi Kattamuri

International Institute of Information Technology, Hyderabad

---

# References

1. *RF Electronics* — Behzad Razavi  
2. *Microelectronic Circuits* — Sedra & Smith  
3. Electronics Tutorials  
4. All About Electronics  
