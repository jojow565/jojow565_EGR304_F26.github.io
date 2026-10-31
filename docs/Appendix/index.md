---
title: Appendix - Main Page
---

# Appendix — Microphone Subsystem

**EGR 304 | Team 203 | Joseph White**

## Overview

This appendix provides supporting technical information for the microphone detection subsystem of the automated cat-toy project.

The subsystem uses the microphone supplied during EGR 304 laboratory exercises, an MCP6004 operational amplifier, and a PIC18F57Q43 Curiosity Nano microcontroller.

## Main Components

| Component | Part Number | Purpose |
|---|---|---|
| Microcontroller | PIC18F57Q43 | Signal processing and communication |
| Microphone | Class-supplied two-wire microphone | Acoustic detection |
| Operational amplifier | MCP6004 | Microphone signal conditioning |
| Potentiometer | XCHC Electron 3296W-103 | Adjustable voltage reference |
| Voltage regulator | LM7805 | Regulated 5 V supply |
| Pushbutton | Momentary switch | User input |
| Indicator LED | Red LED | Visual status indication |

## Microphone Signal Conditioning

The microphone detects acoustic signals and provides an electrical signal to the MCP6004 operational amplifier.

The amplifier conditions the microphone signal before it reaches the microcontroller's analog-to-digital converter (ADC).

A 10 kΩ multiturn potentiometer provides an adjustable reference voltage for the amplifier.

The potentiometer is adjusted to approximately 2.5 V to establish the desired reference level.

### Potentiometer Connections

| Potentiometer Pin | Connection |
|---|---|
| Pin 1 | +5 V |
| Pin 2 (Wiper) | MCP6004 reference input |
| Pin 3 | Ground |

## Microcontroller Pin Configuration

| PIC Pin | Function | Purpose |
|---|---|---|
| RA0 | ADC input | Conditioned microphone signal |
| RA1 | GPIO output | INT_OUT |
| RA2 | DAC output | Analog output |
| RC6 | UART TX | Serial transmission |
| RC7 | UART RX | Serial reception |
| RD1 | GPIO input | Pushbutton |
| RD2 | GPIO output | Red LED |

## Power System

The subsystem uses an external 9–12 V DC supply.

An LM7805 linear voltage regulator provides a regulated 5 V supply for the circuit.

The design uses a single regulated 5 V power rail.

The 10 kΩ potentiometer establishes an adjustable reference voltage of approximately 2.5 V for the amplifier.

No additional 3.3 V regulator is required for the selected design.

## Signal Flow

1. The class-supplied microphone detects sound.
2. The MCP6004 amplifies and conditions the microphone signal.
3. The 10 kΩ potentiometer establishes the amplifier reference voltage.
4. The conditioned signal enters the PIC18F57Q43 through RA0.
5. The microcontroller processes the ADC readings.
6. UART1 provides communication with the other team subsystems.

## Supporting Documentation

### Microcontroller

[PIC18F57Q43 Documentation](https://www.microchip.com/en-us/product/PIC18F57Q43)

### Operational Amplifier

[MCP6004 Documentation](https://www.microchip.com/en-us/product/MCP6004)

## Design Status

The microphone subsystem is currently in the external design review stage.

The design uses the class-supplied microphone, MCP6004 signal-conditioning circuit, adjustable 10 kΩ potentiometer reference, and regulated 5 V power supply.

Final circuit operation will be verified during hardware testing.
```
