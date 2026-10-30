# Bill of Materials — Microphone Subsystem

**EGR 304 | Team 203 | Joseph White**

**Status: Updated — October 30, 2026**

## Overview

This bill of materials (BOM) documents the components included in the microphone detection subsystem schematic.

The subsystem uses a microphone, an MCP6004 operational amplifier for analog signal conditioning, a PIC18F57Q43 Curiosity Nano development board, and an LM7805 regulator for the 5 V power rail.

All schematic components are included, including components already owned and those requiring purchase.

Component quantities represent the requirements for one subsystem assembly. Additional quantities needed for prototyping and replacement parts are listed separately in the purchasing section.

## Bill of Materials

| Description | Qty | Reference | Manufacturer / Part Number | Unit Cost | Availability |
|---|---:|---|---|---:|---|
| Capacitor, 0.33 µF, 25 V | 1 | C1 | TBD | N/A | Owned |
| Capacitor, 0.1 µF, 25 V | 5 | C2, C3, C4, C6, C7 | TBD | N/A | Owned |
| Capacitor, 0.22 µF, 25 V | 1 | C5 | TBD | N/A | Owned |
| Green LED | 1 | D2 | TBD | N/A | Owned |
| Red LED | 1 | D3 | TBD | N/A | Owned |
| Fuse, 1 A, 5 × 20 mm, fast-acting | 1 | F1 | Littelfuse 0217001.MXP | $0.61 | Order |
| Fuse mounting clips | 2 | F1 mounting hardware | Bel Fuse FC-203 BRIGHT TIN | $0.15 | Order |
| DC barrel jack | 1 | J1 | TBD | N/A | Owned |
| 8-pin connector | 1 | J3 | 2.54 mm header, exact part TBD | N/A | Owned |
| Solder jumpers | 2 | JP1, JP2 | PCB solder jumpers | N/A | PCB |
| Microphone | 1 | MK1 | Existing microphone, model TBD | N/A | Owned |
| Resistor, 1 kΩ, ¼ W | 3 | R1, R5, R7 | TBD | N/A | Owned |
| Resistor, 10 kΩ, ¼ W | 5 | R3, R4, R13–R15 | TBD | N/A | Owned |
| Resistor, 2.2 kΩ, ¼ W | 1 | R6 | TBD | N/A | Owned |
| Resistor, 100 kΩ, ¼ W | 1 | R8 | TBD | N/A | Owned |
| Resistor, 220 Ω, ¼ W | 1 | R9 | TBD | N/A | Owned |
| Resistor, 330 Ω, ¼ W | 1 | R10 | TBD | N/A | Owned |
| Resistor, 100 Ω, ¼ W | 2 | R11, R12 | TBD | N/A | Owned |
| Trimmer potentiometer, 10 kΩ | 1 | RV1 | XCHC Electron 3296W-103 | N/A | Owned |
| Momentary pushbutton | 1 | SW1 | TBD | N/A | Owned |
| Test points | 6 | TP1–TP6 | PCB test points | N/A | PCB |
| 5 V linear regulator | 1 | U1 | LM7805, variant TBD | N/A | Owned |
| PIC18F57Q43 Curiosity Nano | 1 | U2 | Microchip PIC18F57Q43 Curiosity Nano | N/A | Owned |
| Quad operational amplifier, DIP-14 | 1 | U3 | Microchip MCP6004-I/P | N/A | Owned |

**Total: 41 schematic component instances across 23 grouped schematic entries, plus 2 fuse mounting clips (24 BOM rows total).**

**Note:** N/A indicates that a component is already owned or is implemented directly on the PCB. It does not indicate that the component has no monetary value.

## Component Selection

### Microphone

The microphone converts acoustic signals into electrical signals for processing by the operational amplifier.

The existing microphone will be used for prototyping. Its exact manufacturer part number and electrical specifications will be verified.

### Operational Amplifier

The MCP6004-I/P is a quad operational amplifier used for analog signal conditioning.

The amplifier increases the microphone signal amplitude before the signal is sampled by the microcontroller ADC.

### Microcontroller

The Microchip PIC18F57Q43 Curiosity Nano development board provides analog-to-digital conversion, digital processing, and digital-to-analog conversion.

The subsystem uses the following signals:

| Signal | PIC Pin | Function |
|---|---|---|
| RA0_ADC | RA0 | Analog microphone input |
| DAC_OUT | RA2 | DAC output |
| INT_OUT | RA1 | Interrupt output |
| UART_RX | RC7 | UART receive |
| UART_TX | RC6 | UART transmit |
| BTN | RD1 | Pushbutton input |
| LED | RD2 | LED output |
| GND | GND | Common ground |

### Potentiometer

The XCHC Electron 3296W-103 is a 10 kΩ multiturn trimmer potentiometer.

The potentiometer provides an adjustable reference voltage for the MCP6004 non-inverting input.

Connections:

- Pin 1: +5 V
- Pin 2: MCP6004 non-inverting input
- Pin 3: GND

KiCad footprint:

`Potentiometer_THT:Potentiometer_Bourns_3296W_Vertical`

The potentiometer is already owned and does not require purchasing.

### Voltage Regulator

The LM7805 provides a regulated 5 V supply for the microphone subsystem.

The regulator is already available and does not require purchasing.

### Fuse and Fuse Holder

A replaceable 1 A fast-acting fuse protects the subsystem power input.

Selected components:

- Fuse: Littelfuse 0217001.MXP
- Fuse clips: Bel Fuse FC-203 BRIGHT TIN
- Fuse dimensions: 5 × 20 mm
- Two mounting clips are required for each fuse.

KiCad footprint:

`Fuse:Fuseholder_Clip-5x20mm_Bel_FC-203-22_Lateral_P17.80x5.00mm_D1.17mm_Horizontal`

The fuse and mounting clips are the only components currently identified for purchase.

## Hardware Availability

The following components are already available and do not require purchasing:

- Microphone
- PIC18F57Q43 Curiosity Nano
- MCP6004 operational amplifier
- LM7805 voltage regulator
- Resistors
- Capacitors
- 10 kΩ potentiometer
- LEDs
- Pushbutton
- DC barrel jack
- Header pins

The solder jumpers and PCB test points are implemented as PCB features and do not require separate component purchases.

## Purchase Requirements

The following components must be ordered from DigiKey.

| Description | Manufacturer | Part Number | Quantity to Order | Unit Cost | Extended Cost |
|---|---|---|---:|---:|---:|
| 1 A fast-acting fuse, 5 × 20 mm | Littelfuse | 0217001.MXP | 3 | $0.61 | $1.83 |
| Fuse mounting clips | Bel Fuse | FC-203 BRIGHT TIN | 4 | $0.15 | $0.60 |
| **Total** | | | | | **$2.43** |

### Purchase Quantity Explanation

**Fuses:**
- 1 fuse required for the subsystem
- 2 additional replacement fuses
- 3 fuses ordered total

**Fuse mounting clips:**
- 2 clips required for the subsystem
- 2 additional clips for spare hardware
- 4 clips ordered total

The estimated component cost is **$2.43**, excluding shipping and applicable taxes.

Prices were checked against DigiKey listings on October 30, 2026.

## Outstanding Items

- Verify the exact microphone model and electrical specifications.
- Verify component footprints against the physical parts.
- Run KiCad Electrical Rules Check (ERC).
- Download and organize manufacturer datasheets.
- Submit the purchase request for instructor approval.

## Design Status

**Updated BOM — component inventory and purchasing requirements confirmed; final schematic verification and instructor purchasing approval pending.**
