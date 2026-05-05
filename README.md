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

A BJT differential amplifier is used as the pre-amplifier stage for inital amplification and for common-mode signal rejection. Designed for a differential gain of 20. Achieved a gain of 21.5 and Common Mode rejection Ratio of 19.53 dB.

---

## 2. Common Emitter Gain Stage

The CE amplifier provides most of the voltage amplification. Designed for a gain of nearly 25. Final resistor values chosen to achive this gain was RC = 7.2 kΩ
and RE = 270 Ω

---

## 3. Active Bandpass Filter

An active bandpass filter restricts the signal to the audible frequency range. Designed for the 3dB cutoff frequencies as lower cutoff at 9.5 Hz and upper cutoff at 39 kHz, with a unity gain . The main purpose is to remove unwanted frequency componenets to preserve the audio quality.

---

## 4. Class AB Power Amplifier

A Class AB push-pull amplifier drives the speaker load. This reduces distortion and is efficient. Diode biasing was used for smooth switching. Power transistor TIP31C and TIP32C were used. 

---

# Results

| Metric | Value |
|---|---|
| Simulated Gain | 430.5 |
| Hardware Gain | 410 |
| Slew Rate | 0.546 V/µs |


---




