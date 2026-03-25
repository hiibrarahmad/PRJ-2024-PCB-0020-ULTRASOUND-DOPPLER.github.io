<div align="center">

<img src="https://raw.githubusercontent.com/hiibrarahmad/PRJ-2024-PCB-0020-ULTRASOUND-DOPPLER.github.io/main/Assets/PRJ-2024-PCB-0020-ULTRASOUND-DOPPLER.github.io-TOP.jpg" width="100%" alt="Ultrasound Doppler PCB - Top View"/>

---

# PRJ-2024-PCB-0020-ULTRASOUND-DOPPLER

### Ultrasonic Doppler Measurement Front-End (USD3.0)

Designed by [Hibrar Ahmad](https://github.com/hiibrarahmad)

[![Project](https://img.shields.io/badge/Project-USD3.0-0ea5e9?style=for-the-badge)](#)
[![MCU](https://img.shields.io/badge/MCU-LPC4330-22c55e?style=for-the-badge)](#)
[![CPLD](https://img.shields.io/badge/CPLD-MachXO2-ef4444?style=for-the-badge)](#)
[![ADC](https://img.shields.io/badge/ADC-AD9245-0ea5e9?style=for-the-badge)](#)
[![USB](https://img.shields.io/badge/USB-Micro--B-f59e0b?style=for-the-badge)](#)
[![Status](https://img.shields.io/badge/Status-Research%20Prototype-64748b?style=for-the-badge)](#)

[![Last Commit](https://img.shields.io/github/last-commit/hiibrarahmad/PRJ-2024-PCB-0020-ULTRASOUND-DOPPLER.github.io?style=for-the-badge&color=0891b2&label=Last%20Commit)](../../commits/main)
[![GitHub Pages](https://img.shields.io/badge/GitHub%20Pages-Live-22c55e?style=for-the-badge&logo=github)](https://hiibrarahmad.github.io/PRJ-2024-PCB-0020-ULTRASOUND-DOPPLER.github.io/)

<br/>

[Interactive PCB View](https://hiibrarahmad.github.io/PRJ-2024-PCB-0020-ULTRASOUND-DOPPLER.github.io/) ? [Project Assets](https://github.com/hiibrarahmad/PRJ-2024-PCB-0020-ULTRASOUND-DOPPLER.github.io/tree/main/Assets) ? [Specification PDF](https://github.com/hiibrarahmad/PRJ-2024-PCB-0020-ULTRASOUND-DOPPLER.github.io/blob/main/Assets/PRJ-2024-PCB-0020-ULTRASOUND-DOPPLER-Spec.pdf)

</div>

---

## Contents

1. Overview
2. PCB Preview
3. System Summary
4. Key Specifications
5. Key Components
6. Interfaces and Debug
7. Power Domains
8. Documents and Downloads
9. Interactive BOM
10. Repository Structure
11. Safety Notice
12. Links

---

## Overview

**PRJ-2024-PCB-0020-ULTRASOUND-DOPPLER** (USD3.0) is a USB-controlled ultrasonic Doppler measurement front-end. It excites a piezoelectric transducer, receives Doppler-shifted echoes, filters and amplifies the signal, digitizes it, and streams data for analysis.

---

## PCB Preview

<table>
<tr>
<td align="center" width="50%">

**Top Side**

<img src="https://raw.githubusercontent.com/hiibrarahmad/PRJ-2024-PCB-0020-ULTRASOUND-DOPPLER.github.io/main/Assets/PRJ-2024-PCB-0020-ULTRASOUND-DOPPLER.github.io-TOP.jpg" width="100%" alt="Ultrasound Doppler PCB - Top View"/>

</td>
<td align="center" width="50%">

**Bottom Side**

<img src="https://raw.githubusercontent.com/hiibrarahmad/PRJ-2024-PCB-0020-ULTRASOUND-DOPPLER.github.io/main/Assets/PRJ-2024-PCB-0020-ULTRASOUND-DOPPLER.github.io-BOT.jpg" width="100%" alt="Ultrasound Doppler PCB - Bottom View"/>

</td>
</tr>
</table>

---

## System Summary

Signal chain overview (schematics-based):

- CPLD generates TX timing and gating signals.
- Differential line driver excites the piezo transducer via RF transformers.
- Echo returns through band-pass filtering and protection network.
- Differential RF/IF amplifier drives a 14-bit ADC.
- MCU handles control and USB communication.

---

## Key Specifications

| Parameter | Value |
|----------|-------|
| Band-pass response | f_low ~ 140 kHz, f_high ~ 9.8 MHz (schematic note) |
| Insertion loss | ~ -1.4 dB at 8 MHz (schematic note) |
| ADC | AD9245BCPZ-80, 14-bit differential |
| MCU clock | 12 MHz crystal |
| CPLD clock | 64 MHz oscillator |
| Supported transducers | 4 MHz and 8 MHz (2 MHz with added series resistance) |
| Interfaces | USB Micro-B, USB-A male/female, SWD/JTAG |

---

## Key Components

| Function | Component |
|---------|-----------|
| MCU | NXP LPC4330 (Cortex-M4) |
| CPLD | Lattice MachXO2-7000HC |
| ADC | AD9245 (14-bit) |
| RX amplifier | AD8351 (RF/IF differential) |
| TX driver | AD8018 (high-speed differential) |
| Power mux | TPS2115A |
| Regulators | L78M05, ADP151, ADP7104 |

---

## Interfaces and Debug

- USB Micro-B for data and power input.
- USB-A male and USB-A female connectors for system routing.
- External power jack (NETPW).
- SWD/JTAG headers for MCU and CPLD programming/debug.
- Test points distributed across key rails and signals.

---

## Power Domains

- TXD5V0: Regulated 5 V for transmitter path.
- VDD5V0: 5 V domain from muxed input.
- RXA3V3: 3.3 V analog for receiver and ADC.
- VDD3V3: 3.3 V digital for MCU and CPLD.
- Separate grounds for power, digital, and analog sections.

---

## Documents and Downloads

| Document | Location |
|----------|----------|
| Specification PDF | Assets/PRJ-2024-PCB-0020-ULTRASOUND-DOPPLER-Spec.pdf |
| Interactive BOM | index.html (GitHub Pages) |
| PCB Renders | Assets/ (Top/Bottom PNG/JPG) |

---

## Interactive BOM

Open the live viewer:
https://hiibrarahmad.github.io/PRJ-2024-PCB-0020-ULTRASOUND-DOPPLER.github.io/

---

## Repository Structure

```
PRJ-2024-PCB-0020-ULTRASOUND-DOPPLER.github.io/
|
|-- Assets/
|   |-- PRJ-2024-PCB-0020-ULTRASOUND-DOPPLER.github.io-TOP.jpg
|   |-- PRJ-2024-PCB-0020-ULTRASOUND-DOPPLER.github.io-BOT.jpg
|   |-- PRJ-2024-PCB-0020-ULTRASOUND-DOPPLER.github.io-TOP.png
|   |-- PRJ-2024-PCB-0020-ULTRASOUND-DOPPLER.github.io-BOT.png
|   |-- PRJ-2024-PCB-0020-ULTRASOUND-DOPPLER-Spec.pdf
|
|-- index.html
|-- .gitattributes
|-- README.md
```

---

## Safety Notice

This project is a research hardware platform and is not a certified medical device. Use appropriate precautions and follow applicable regulations for any clinical or safety-critical usage.

---

## Links

| Resource | URL |
|----------|-----|
| Interactive PCB View | https://hiibrarahmad.github.io/PRJ-2024-PCB-0020-ULTRASOUND-DOPPLER.github.io/ |
| Specification PDF | https://github.com/hiibrarahmad/PRJ-2024-PCB-0020-ULTRASOUND-DOPPLER.github.io/blob/main/Assets/PRJ-2024-PCB-0020-ULTRASOUND-DOPPLER-Spec.pdf |
| Designer | https://github.com/hiibrarahmad |
| Top View | https://github.com/hiibrarahmad/PRJ-2024-PCB-0020-ULTRASOUND-DOPPLER.github.io/blob/main/Assets/PRJ-2024-PCB-0020-ULTRASOUND-DOPPLER.github.io-TOP.jpg |
| Bottom View | https://github.com/hiibrarahmad/PRJ-2024-PCB-0020-ULTRASOUND-DOPPLER.github.io/blob/main/Assets/PRJ-2024-PCB-0020-ULTRASOUND-DOPPLER.github.io-BOT.jpg |

---

<div align="center">

**PRJ-2024-PCB-0020-ULTRASOUND-DOPPLER**

Ultrasonic Doppler Measurement Front-End

Copyright 2026 ibrar Ahmad (hiibrarahmad). All Rights Reserved.

</div>
