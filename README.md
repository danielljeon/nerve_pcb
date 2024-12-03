# nerve_pcb

![kibot](https://github.com/danielljeon/nerve_pcb/actions/workflows/kibot.yaml/badge.svg)

Nerve production board for complete application integration

| Top                                          | Bottom                                             |
|----------------------------------------------|----------------------------------------------------|
| ![nerve_pcb-top.png](docs/nerve_pcb-top.png) | ![nerve_pcb-bottom.png](docs/nerve_pcb-bottom.png) |

---

<details markdown="1">
  <summary>Table of Contents</summary>

<!-- TOC -->
* [nerve_pcb](#nerve_pcb)
  * [1 Overview](#1-overview)
    * [1.1 Connectors](#11-connectors)
    * [1.2 Switches & Jumpers](#12-switches--jumpers)
<!-- TOC -->

</details>

---

## 1 Overview

Production optimized PCB for the STM32
based [nerve](https://github.com/danielljeon/nerve) controller firmware.

### 1.1 Connectors

Connectors fixed by hardware (PCB traces or the connector itself).

| Connector                       | Ref | Description                                                                    |
|---------------------------------|:---:|--------------------------------------------------------------------------------|
| Tag-Connect TC2050              | J1  | Programming/debug connector                                                    |
| USB-C 5 V Power                 | J2  | Power only USB-C, primary 5 V source                                           |
| BOOT0 Jumper                    | J3  | Open for run flash memory (pull-down on open)                                  |
| Hinge microSD Card              | J4  | Portable storage, see [Molex product video](https://youtu.be/YY2V8z6UK7M?t=95) |
| Top side 2x8 board-to-board     | J5  | See schematic/layout for details                                               |
| Bottom side 2x15 board-to-board | J6  | See schematic/layout for details                                               |
| CAN1 (Transceiver U7)           | J7  | Pin 1: CAN1 High, Pin 2: CAN1 Low                                              |
| CAN2 (Transceiver U8)           | J8  | Pin 1: CAN2 High, Pin 2: CAN2 Low                                              |

### 1.2 Switches & Jumpers

User controllable hardware and/or firmware driven inputs.

| Switch/Jumper           | Ref | Description                                      |
|-------------------------|:---:|--------------------------------------------------|
| MCU NRESET Switch       | SW1 | Generic 6 mm TH button, push to reset            |
| MCU PA0 Switch          | SW2 | Generic 6 mm TH button, designed for SYS_WKUP0   |
| MCU Vbatt               | JP1 | Bridge to short 3.3 V supply to Vbatt            |
| SDIO Card Detect Jumper | JP2 | Bridge for card not inserted (pull-down on open) |
| BMP390 I2C Address      | JP3 | Bridge for `0x76` (pull-down on open, `0x77`)    |
