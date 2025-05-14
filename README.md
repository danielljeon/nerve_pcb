# nerve_pcb

![kibot](https://github.com/danielljeon/nerve_pcb/actions/workflows/kibot.yaml/badge.svg)

PCB for CAN-based control systems dev platform.

- Firmware: [`nerve`](https://github.com/danielljeon/nerve).

---

<details markdown="1">
  <summary>Table of Contents</summary>

<!-- TOC -->
* [nerve_pcb](#nerve_pcb)
  * [1 Overview](#1-overview)
  * [2 Board Specifications](#2-board-specifications)
    * [2.1 Connectors](#21-connectors)
    * [2.2 Switches & Jumpers](#22-switches--jumpers)
  * [3 Release Notes](#3-release-notes)
    * [3.1 v0.1.0-alpha](#31-v010-alpha)
    * [3.2 v0.1.0-beta](#32-v010-beta)
    * [3.3 v0.1.0 (WIP)](#33-v010-wip)
  * [💖 Sponsors](#-sponsors)
    * [PCBWay](#pcbway)
      * [Why PCBWay?](#why-pcbway)
<!-- TOC -->

</details>

---

<a href="https://www.pcbway.com">
  <img src="docs/PCBWay.svg" alt="PCBWay Logo" style="width:25%;" />
</a>

This project is sponsored by **PCBWay**. You can learn more about their valuable
support here: [💖 Sponsors/PCBWay](#pcbway).

---

## 1 Overview

|                               Top                               |                                Bottom                                 |
|:---------------------------------------------------------------:|:---------------------------------------------------------------------:|
|          ![nerve_pcb-top.png](docs/nerve_pcb-top.png)           |          ![nerve_pcb-bottom.png](docs/nerve_pcb-bottom.png)           |
| ![4layer_variant_top.png](docs/pictures/4layer_variant_top.png) | ![4layer_variant_bottom.png](docs/pictures/4layer_variant_bottom.png) |

- Bottom row pictures show 4 Layer assembly variant of `nerve_pcb`,
  v0.1.0-alpha.

---

## 2 Board Specifications

### 2.1 Connectors

Connectors fixed by hardware (PCB traces or the connector itself).

| Connector                       | Ref | Description                                                                    |
|---------------------------------|:---:|--------------------------------------------------------------------------------|
| Tag-Connect TC2050              | J1  | Programming/debug connector                                                    |
| USB-C 5 V power                 | J2  | Power only USB-C, primary 5 V source                                           |
| BOOT0 jumper                    | J3  | Open for run flash memory (pull-down on open)                                  |
| Hinge microSD card              | J4  | Portable storage, see [Molex product video](https://youtu.be/YY2V8z6UK7M?t=95) |
| Top side 2x8 board-to-board     | J5  | See schematic/layout for details                                               |
| Bottom side 2x10 board-to-board | J6  | See schematic/layout for details                                               |
| UART3                           | J7  | Pin 1: UART3 RX, Pin 2: UART3 TX                                               |
| CAN1 (Transceiver U7)           | J8  | Pin 1: CAN1 High, Pin 2: CAN1 Low                                              |
| CAN2 (Transceiver U8)           | J9  | Pin 1: CAN2 High, Pin 2: CAN2 Low                                              |

### 2.2 Switches & Jumpers

User controllable hardware and/or firmware driven inputs.

| Switch/Jumper           | Ref | Description                                    |
|-------------------------|:---:|------------------------------------------------|
| MCU NRESET switch       | SW1 | Generic 6 mm TH button, push to reset          |
| MCU PA0 switch          | SW2 | Generic 6 mm TH button, designed for SYS_WKUP0 |
| MCU 3.3VBATT            | JP1 | Bridge to short 3.3 V supply to MCU VBAT       |
| SDIO card detect jumper | JP2 | Open = card detected, closed = not detected    |
| BNO085 clock select     | JP3 | Open = crystal, closed = external/internal     |
| BMP390 I2C address      | JP4 | Open = `0x76`, closed = `0x77`                 |

---

## 3 Release Notes

### 3.1 v0.1.0-alpha

- Pre-release 4-layer development board variant.
- `nerve_pcb_dev`, commit 76bec6f.
    - Original commit on a different repo for automated workflow reasons.
    - Closest commit on this repo
      is [f2d1f21](https://github.com/danielljeon/nerve_pcb/commit/f2d1f21cb11d7a693d17076e7c4d2955f681dbfa).
- Order date: 2024/11/15.
- Order number: `W837000ASB3`.

### 3.2 v0.1.0-beta

- Pre-release 6-layer board variant.
    - Short-term pre-release board bring-up/testing release.
- Order date: 2025/01/13.

### 3.3 v0.1.0 (WIP)

- Minor changes from the previous `v0.1.0-beta` pre-release version.
    - CAN termination design switched from single 120 ohm termination to split
      60 ohm termination with 4.7 nF capacitor.

---

## 💖 Sponsors

### PCBWay

<a href="https://www.pcbway.com">
  <img src="docs/PCBWay.svg" alt="PCBWay Logo" style="width:25%;" />
</a>

This project is sponsored by [**PCBWay**](https://www.pcbway.com), whose PCB
manufacturing services are essential in producing high-quality prototypes for
its development. Their support ensures reliable boards that meet the project's
demands.

#### Why PCBWay?

PCBWay stands out for their exceptional services and commitment to the
community:

- **PCB Manufacturing**: High-quality fabrication with options for multilayer,
  rigid-flex, and advanced designs.
- **PCB Assembly**: Comprehensive solutions, including soldering, component
  sourcing, and assembly.
- **CNC Machining & 3D Printing**: Additional prototyping options to support
  complete product development.
- **Fast Turnaround**: Reliable and quick production times to keep projects on
  schedule.
- **Support for Open Source & Education**: PCBWay actively sponsors projects and
  provides educational resources like tutorials, videos, and documentation,
  empowering developers and hobbyists.
    - This commitment to education and open-source advocacy was a key factor in
      choosing them as a partner 🙂.

Their dedication to professional-grade services and fostering innovation makes
PCBWay an invaluable partner in bringing this project to life.

Learn more here: [Why PCBWay?](https://www.pcbway.com/why.html)
