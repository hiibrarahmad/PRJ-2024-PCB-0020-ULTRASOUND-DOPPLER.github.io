<div align="center">

<img src="https://raw.githubusercontent.com/hiibrarahmad/PRJ-2024-PCB-0020-ULTRASOUND-DOPPLER.github.io/main/Assets/PRJ-2024-PCB-0020-ULTRASOUND-DOPPLER.github.io-TOP.jpg" width="100%" alt="Ultrasound Doppler PCB - Top View"/>

---

# PRJ-2024-PCB-0020-ULTRASOUND-DOPPLER

### Ultrasonic Doppler Measurement Front-End (USD3.0)

**Designed by [Hibrar Ahmad](https://github.com/hiibrarahmad)**

[![PCB Version](https://img.shields.io/badge/PCB%20Version-USD3.0-00c8ff?style=for-the-badge)](#)
[![MCU](https://img.shields.io/badge/MCU-LPC4330-22c55e?style=for-the-badge)](#)
[![CPLD](https://img.shields.io/badge/CPLD-MachXO2-ef4444?style=for-the-badge)](#)
[![ADC](https://img.shields.io/badge/ADC-AD9245-0ea5e9?style=for-the-badge)](#)
[![USB](https://img.shields.io/badge/USB-Micro--B-f59e0b?style=for-the-badge)](#)
[![Transducer](https://img.shields.io/badge/Transducer-4%20%2F%208%20MHz-a855f7?style=for-the-badge)](#)

[![Last Commit](https://img.shields.io/github/last-commit/hiibrarahmad/PRJ-2024-PCB-0020-ULTRASOUND-DOPPLER.github.io?style=for-the-badge&color=0891b2&label=Last%20Commit)](../../commits/main)
[![GitHub Pages](https://img.shields.io/badge/GitHub%20Pages-Live-22c55e?style=for-the-badge&logo=github)](https://hiibrarahmad.github.io/PRJ-2024-PCB-0020-ULTRASOUND-DOPPLER.github.io/)
[![Visitors](https://visitor-badge.laobi.icu/badge?page_id=hiibrarahmad.PRJ-2024-PCB-0020-ULTRASOUND-DOPPLER.github.io&style=for-the-badge&color=0e7490)](https://github.com/hiibrarahmad/PRJ-2024-PCB-0020-ULTRASOUND-DOPPLER.github.io)

<br/>

[Interactive PCB View](https://hiibrarahmad.github.io/PRJ-2024-PCB-0020-ULTRASOUND-DOPPLER.github.io/) ? [Project Assets](https://github.com/hiibrarahmad/PRJ-2024-PCB-0020-ULTRASOUND-DOPPLER.github.io/tree/main/Assets) ? [Specification PDF](https://github.com/hiibrarahmad/PRJ-2024-PCB-0020-ULTRASOUND-DOPPLER.github.io/blob/main/Assets/PRJ-2024-PCB-0020-ULTRASOUND-DOPPLER-Spec.pdf)

</div>

---

## Project Overview

**PRJ-2024-PCB-0020-ULTRASOUND-DOPPLER** (USD3.0) is a USB-controlled ultrasonic Doppler measurement front-end. It drives a piezoelectric transducer, receives Doppler-shifted echoes, filters and amplifies the signal, digitizes it, and streams data for analysis.

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

<div align="center">

**View the Interactive PCB Online:**
https://hiibrarahmad.github.io/PRJ-2024-PCB-0020-ULTRASOUND-DOPPLER.github.io/

</div>

---

## Core Design Goals

| Goal | Specification |
|------|--------------|
| Ultrasonic Front-End | Differential TX/RX signal chain for Doppler measurement |
| MCU | NXP LPC4330 (Cortex-M4) control and USB communication |
| CPLD | Lattice MachXO2 timing/state machine |
| ADC | AD9245, 14-bit differential input |
| Band-pass | 140 kHz to 9.8 MHz (per schematic notes) |
| Transducer | 4 MHz / 8 MHz supported (2 MHz with added series resistance) |
| Power | USB or external input with regulated 5 V and 3.3 V rails |

---

## Key Specifications

| Parameter | Value |
|----------|-------|
| Band-pass response | f_low ~ 140 kHz, f_high ~ 9.8 MHz |
| Insertion loss | ~ -1.4 dB at 8 MHz (schematic note) |
| ADC | AD9245BCPZ-80, 14-bit differential |
| MCU clock | 12 MHz crystal |
| CPLD clock | 64 MHz oscillator |
| Power rails | TXD5V0, VDD5V0, RXA3V3, VDD3V3 |
| Interfaces | USB Micro-B, USB-A male/female, SWD/JTAG |

---

## Interfaces

- USB Micro-B (USB0 data + VBUS)
- USB-A female and USB-A male (system overview)
- External power jack (NETPW)
- SWD/JTAG headers for MCU and CPLD

---

## Interactive BOM

The Interactive BOM is available in the live page:
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

*Ultrasonic Doppler Measurement Front-End*  

Copyright 2026 Hibrar Ahmad. All Rights Reserved.

</div>
