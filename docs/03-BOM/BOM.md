---
title: Bill of Materials
tags:
- BOM
- microphone
- hardware
---

# Bill of Materials — Microphone Subsystem

**EGR 304 | Team 203 | Joseph White**

**Status: Updated — November 25, 2026**

## Overview

This bill of materials (BOM) documents the components used in the manufactured microphone detection subsystem.

The subsystem uses a two-wire electret condenser microphone, a Microchip MCP6004-I/P operational amplifier for analog signal conditioning, a PIC18F57Q43 Curiosity Nano development board, and an STMicroelectronics L7805ABV voltage regulator.

Power is supplied by an external model 0930 AC/DC wall adapter rated at 9 V DC and 3 A.

Component quantities represent the requirements for one subsystem assembly. Additional components identified for replacement and prototyping are listed separately in the purchasing section.

## Bill of Materials

| Description | Qty | Reference | Manufacturer / Part Number | Unit Cost | Availability |
|---|---:|---|---|---:|---|
| Capacitor, 0.33 µF, 25 V | 1 | C1 | Unidentified | N/A | Owned |
| Capacitor, 0.1 µF, 25 V | 5 | C2, C3, C4, C6, C7 | Unidentified | N/A | Owned |
| Capacitor, 0.22 µF, 25 V | 1 | C5 | Unidentified | N/A | Owned |
| Green LED | 1 | D2 | Generic | N/A | Owned |
| Red LED | 1 | D3 | Generic | N/A | Owned |
| Fuse, 1 A, 5 × 20 mm, fast-acting | 1 | F1 | Littelfuse 0217001.MXP | $0.61 | Selected |
| Fuse mounting clips | 2 | F1 mounting hardware | Bel Fuse FC-203 BRIGHT TIN | $0.15 | Selected |
| DC barrel jack | 1 | J1 | Generic | N/A | Owned |
| 8-pin connector | 1 | J3 | 2.54 mm header | N/A | Owned |
| Solder jumpers | 2 | JP1, JP2 | PCB solder jumpers | N/A | PCB |
| Two-wire electret condenser microphone | 1 | MK1 | Manufacturer and model unidentified | N/A | Owned |
| Resistor, 1 kΩ, ¼ W | 3 | R1, R5, R7 | Generic | N/A | Owned |
| Resistor, 10 kΩ, ¼ W | 5 | R3, R4, R13–R15 | Generic | N/A | Owned |
| Resistor, 2.2 kΩ, ¼ W | 1 | R6 | Generic | N/A | Owned |
| Resistor, 100 kΩ, ¼ W | 1 | R8 | Generic | N/A | Owned |
| Resistor, 220 Ω, ¼ W | 1 | R9 | Generic | N/A | Owned |
| Resistor, 330 Ω, ¼ W | 1 | R10 | Generic | N/A | Owned |
| Resistor, 100 Ω, ¼ W | 2 | R11, R12 | Generic | N/A | Owned |
| Trimmer potentiometer, 10 kΩ | 1 | RV1 | XCHC Electron 3296W-103 | N/A | Owned |
| Momentary pushbutton | 1 | SW1 | Generic | N/A | Owned |
| Test points | 6 | TP1–TP6 | PCB test points | N/A | PCB |
| 5 V linear voltage regulator | 1 | U1 | STMicroelectronics L7805ABV | N/A | Owned |
| PIC18F57Q43 Curiosity Nano | 1 | U2 | Microchip PIC18F57Q43 Curiosity Nano | N/A | Owned |
| Quad operational amplifier, DIP-14 | 1 | U3 | Microchip MCP6004-I/P | N/A | Owned |
| External AC/DC wall adapter, 9 V / 3 A | 1 | External | Model 0930, unbranded | N/A | Owned |
| Custom printed circuit board | 1 | PCB | FR-4, two-layer PCB | N/A | Manufactured |

**Note:** N/A indicates that the component was already available or is implemented directly on the PCB. It does not indicate that the component has no monetary value.

Capacitor values listed in this BOM represent the specified schematic values.

---

## Major Component Specifications

### Microphone

The implemented microphone is a two-wire electret condenser microphone.

The microphone converts acoustic signals into electrical signals for processing by the MCP6004 operational amplifier.

| Characteristic | Specification |
|---|---|
| Reference | MK1 |
| Type | Electret condenser |
| Output | Analog |
| Connections | Two-wire |
| Manufacturer | Unidentified |
| Part number | Unidentified |
| Bias supply | 5 V rail through R6 |
| Bias resistor | 2.2 kΩ |

The microphone was already available and was selected instead of the original MEMS microphone candidates.

The implemented microphone circuit does not require a separate 3.3 V regulator.

### Operational Amplifier

| Characteristic | Specification |
|---|---|
| Reference | U3 |
| Manufacturer | Microchip Technology |
| Part number | MCP6004-I/P |
| Type | Quad operational amplifier |
| Package | DIP-14 |
| Operating supply | 5 V |
| Gain-bandwidth product | 1 MHz |
| Input/output | Rail-to-rail |

The MCP6004 amplifies the microphone signal before it reaches the low-pass filter and microcontroller ADC.

[Microchip MCP6004 Product Information](https://www.microchip.com/en-us/product/MCP6004)

### Voltage Regulator

| Characteristic | Specification |
|---|---|
| Reference | U1 |
| Manufacturer | STMicroelectronics |
| Part number | L7805ABV |
| Type | Linear voltage regulator |
| Package | TO-220 |
| Nominal input voltage | 9 V DC |
| Output voltage | 5 V DC |
| Rated output current | Up to 1.5 A, subject to thermal limitations |

The L7805ABV provides the regulated 5 V supply used by the microphone bias circuit, operational amplifier, microcontroller, and indicator LEDs.

[STMicroelectronics L78 Series Datasheet](https://www.st.com/resource/en/datasheet/l78.pdf)

### External Power Supply

| Characteristic | Specification |
|---|---|
| Manufacturer | Unbranded |
| Model | 0930 |
| Type | AC/DC wall adapter |
| AC input | 100–240 VAC |
| Input frequency | 50/60 Hz |
| DC output | 9 V |
| Rated output current | 3 A |
| Rated output power | 27 W |
| Connector polarity | Center positive |

The external power supply connects to the subsystem through barrel jack J1.

The power architecture is:

**9 V DC Wall Adapter → J1 → 1 A Fuse → L7805ABV → Regulated 5 V Supply**

The adapter's 3 A rating represents its available output current, not the actual current consumed by the subsystem.

### Microcontroller

| Characteristic | Specification |
|---|---|
| Reference | U2 |
| Manufacturer | Microchip Technology |
| Part number | PIC18F57Q43 |
| Development board | Curiosity Nano |
| Configured clock | 64 MHz |
| ADC resolution | 12-bit |
| DAC resolution | 8-bit |
| Communication | UART |
| Programming | USB onboard debugger |

[Microchip PIC18F57Q43 Product Information](https://www.microchip.com/en-us/product/PIC18F57Q43)

### Microcontroller Pin Assignments

| Signal | PIC Pin | Function |
|---|---|---|
| RA0_ADC | RA0 | Analog microphone input |
| DAC_OUT | RA2 | Analog DAC output |
| INT_OUT | RA1 | Digital output |
| UART_TX | RC6 | Team UART transmit |
| UART_RX | RC7 | Team UART receive |
| BTN | RD1 | PCB pushbutton input |
| LED | RD2 | PCB red LED output |
| NANO_BUTTON | RB4 | Nano pushbutton |
| NANO_LED | RF3 | Nano yellow LED |
| UART3_TX | RF0 | PuTTY serial transmit |
| UART3_RX | RF1 | PuTTY serial receive |
| GND | GND | Common ground |

The microcontroller configuration supports microphone signal acquisition, analog output, serial communication, and independent operation of the PCB and Nano pushbuttons and LEDs.

### Potentiometer

The XCHC Electron 3296W-103 is a 10 kΩ multiturn trimmer potentiometer.

The potentiometer provides an adjustable reference voltage for the MCP6004 non-inverting input, allowing adjustment of the amplifier's DC operating point.

Connections:

- Pin 1: +5 V
- Pin 2: MCP6004 non-inverting input
- Pin 3: GND

KiCad footprint:

`Potentiometer_THT:Potentiometer_Bourns_3296W_Vertical`

### Fuse and Fuse Holder

A replaceable 1 A fast-acting fuse provides input power protection.

| Component | Manufacturer | Part Number |
|---|---|---|
| Fuse | Littelfuse | 0217001.MXP |
| Fuse mounting clips | Bel Fuse | FC-203 BRIGHT TIN |

Fuse dimensions: 5 × 20 mm.

Two mounting clips are required for each fuse.

KiCad footprint:

`Fuse:Fuseholder_Clip-5x20mm_Bel_FC-203-22_Lateral_P17.80x5.00mm_D1.17mm_Horizontal`

---

## PCB Specifications

| Characteristic | Specification |
|---|---|
| Board material | FR-4 |
| Copper layers | 2 |
| Board thickness | 1.6 mm |
| Copper weight | 1 oz |
| Solder mask | Green |
| Design software | KiCad |
| Assembly method | Manual soldering |

The custom PCB contains the microphone signal-conditioning circuit, power regulation circuit, microcontroller connections, debug components, test points, and eight-pin team connector.

[PCB Design](../06-PCB-Design/pcb-design.md)

---

## Original Purchasing Requirements

The following components were identified for purchase during the original hardware ordering phase.

| Description | Manufacturer | Part Number | Quantity | Unit Cost | Extended Cost |
|---|---|---|---:|---:|---:|
| 1 A fast-acting fuse, 5 × 20 mm | Littelfuse | 0217001.MXP | 3 | $0.61 | $1.83 |
| Fuse mounting clips | Bel Fuse | FC-203 BRIGHT TIN | 4 | $0.15 | $0.60 |
| **Total** | | | | | **$2.43** |

### Purchase Quantity Explanation

**Fuses:**

- One fuse required for subsystem assembly.
- Two additional replacement fuses.
- Three fuses total.

**Fuse mounting clips:**

- Two clips required for subsystem assembly.
- Two additional spare clips.
- Four clips total.

The original estimated purchase cost was **$2.43**, excluding shipping and applicable taxes.

Prices were recorded from DigiKey listings on October 30, 2026.

This amount represents the original component purchase requirement, not the total replacement value of the assembled subsystem.

---

## Hardware Verification

The microphone subsystem PCB was manufactured, assembled, programmed, and tested.

Hardware verification included the microphone signal-conditioning circuit and microcontroller functionality.

The verification firmware supports:

- Microphone ADC acquisition on RA0.
- Conversion of 12-bit ADC data to an 8-bit DAC value.
- Analog DAC output on RA2.
- UART communication.
- PuTTY serial debugging.
- PCB pushbutton and LED operation.
- Nano pushbutton and LED operation.

Individual subsystem hardware verification was demonstrated to the instructor on November 25, 2026.

[Microcontroller Code](../07-Microcontroller-Code/microcontroller-code.md)

## Design Status

**Individual Hardware Verification Complete**

The subsystem has progressed from component selection and preliminary design to PCB manufacturing, assembly, firmware development, and hardware verification.

Final team communication and subsystem integration remain separate development activities.

The exact manufacturer and model of the existing electret microphone remain unidentified.

---

## Related Documentation

- [Block Diagram](../01-Block-Diagram/Block-Diagram.md)
- [Component Selection](../02-Component-Selection/Component-Selection.md)
- [Electrical Schematic](../04-Schematic/schematic.md)
- [Power Budget](../05-Power-Budget/Power-Budget.md)
- [PCB Design](../06-PCB-Design/pcb-design.md)
- [Microcontroller Code](../07-Microcontroller-Code/microcontroller-code.md)
