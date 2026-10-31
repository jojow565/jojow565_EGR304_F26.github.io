---
title: Schematic
---

# Microphone Subsystem Schematic

**EGR 304 | Team 203 | Joseph White**

## Overview

This schematic represents the microphone detection subsystem designed for the EGR 304 automated cat-toy project at Arizona State University.

The subsystem uses a class-supplied microphone, MCP6004 operational amplifier, adjustable 10 kΩ potentiometer, and PIC18F57Q43 Curiosity Nano microcontroller.

## Circuit Components

The schematic includes:

- **Power Supply:** External 9–12 V DC input, 1 A fuse, and LM7805 linear voltage regulator providing a regulated 5 V supply.
- **Microphone:** Class-supplied microphone for acoustic signal detection.
- **Operational Amplifier:** MCP6004 for microphone signal amplification and conditioning.
- **Potentiometer:** 10 kΩ adjustable potentiometer providing an approximately 2.5 V reference voltage.
- **Low-Pass Filter:** Resistor-capacitor network for filtering the conditioned microphone signal.
- **Microcontroller:** PIC18F57Q43 Curiosity Nano for ADC sampling and digital processing.
- **UART Interface:** TX and RX connections for communication with the team's main controller.
- **Debugging Components:** Pushbutton, indicator LEDs, and test points.

## Schematic

The complete microphone subsystem schematic is displayed below.

![EGR 304 Microphone Subsystem Schematic](EGR304_JW_Microphone_Subsystem.svg)

**Figure 1:** Complete microphone subsystem schematic showing power regulation, signal conditioning, microcontroller connections, and communication interface.

### PDF Version

The schematic is also available as a PDF for detailed viewing and printing.

[View or Download Microphone Subsystem Schematic (PDF)](EGR304_JW_Microphone_Subsystem.pdf)

## Microcontroller Connections

| PIC Pin | Signal | Purpose |
|---|---|---|
| RA0 | RA0_ADC | Conditioned microphone signal |
| RA1 | INT_OUT | Interrupt output |
| RA2 | DAC_OUT | Analog output |
| RC6 | UART_TX | Serial transmit |
| RC7 | UART_RX | Serial receive |
| RD1 | BTN | Pushbutton input |
| RD2 | LED | Red indicator LED |

## Team Connector

The subsystem uses an 8-pin connector for communication and integration with the other team subsystems.

| Connector Pin | Signal | Purpose |
|---|---|---|
| 1 | DAC_OUT | Analog output |
| 2 | RA0_ADC | Microphone ADC signal |
| 3 | UART_TX | Serial transmit |
| 4 | UART_RX | Serial receive |
| 5 | INT_OUT | Interrupt output |
| 6 | BTN | Pushbutton |
| 7 | LED | Indicator LED |
| 8 | GND | Ground |

## Resources

### Schematic PDF

[Download Schematic (PDF)](EGR304_JW_Microphone_Subsystem.pdf)

### Schematic SVG

[View Schematic (SVG)](EGR304_JW_Microphone_Subsystem.svg)

### KiCad Project Files

[Download KiCad Project (ZIP)](EGR304_JW_Microphone_Subsystem.zip)

## Design Status

The schematic documents the microphone subsystem's preliminary external design review configuration.

The design uses a single regulated 5 V supply and includes the class-supplied microphone and adjustable reference potentiometer.

Final hardware operation will be verified during circuit assembly and testing.
```
