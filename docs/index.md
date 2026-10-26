
# EGR 304 — Embedded Systems Design

<center>

# Joseph White — Individual Engineering Datasheet

### Microphone Detection Subsystem

**Team 203 | Fall 2026**

**External Design Review — October 26, 2026**

</center>

## Introduction

This individual engineering datasheet documents my design and development work for EGR 304 — Embedded Systems Design at Arizona State University.

My assigned subsystem focuses on detecting and conditioning an audio signal from a microphone so that it can be processed by a PIC18F57Q43 microcontroller.

This website serves as a living engineering document containing the design decisions, component selections, electrical schematics, power calculations, and supporting documentation for the subsystem.

## Project Overview

The microphone detection subsystem is designed to receive an acoustic signal, condition the signal using analog circuitry, and provide a suitable electrical signal to the microcontroller for processing.

The proposed design includes:

- A microphone for converting sound into an electrical signal.
- An MCP6004 operational amplifier for analog signal conditioning.
- Resistors and capacitors for signal filtering and biasing.
- A PIC18F57Q43 Curiosity Nano development board for signal processing.
- An LM7805 voltage regulator providing a regulated 5 V supply.
- An external 9–12 V DC power source.

The design is currently in the preliminary development stage. Final component specifications and operating limits will be confirmed through datasheet verification and testing.

## My Individual Contribution

My responsibilities for the microphone detection subsystem include:

- Developing and documenting the subsystem block diagram.
- Researching and evaluating electrical components.
- Preparing the bill of materials (BOM).
- Designing the electrical schematic.
- Developing the preliminary subsystem power budget.
- Evaluating component compatibility, power requirements, and design constraints.
- Maintaining engineering documentation for design reviews.

## System Operation

The intended signal path is:

**Acoustic Input → Microphone → Analog Signal Conditioning → PIC18F57Q43 Microcontroller**

The microphone produces an electrical signal corresponding to the incoming sound. The analog conditioning circuit amplifies and filters the signal before it reaches the microcontroller.

The microcontroller can then sample the conditioned signal using its analog-to-digital converter (ADC).

## Project Documentation

The following sections contain the supporting engineering documentation:

- [Block Diagram](01-Block-Diagram/Block-Diagram.md)
- [Component Selection](02-Component-Selection/Component-Selection.md)
- [Bill of Materials](03-BOM/BOM.md)
- [Schematic](04-Schematic/Schematic.md)
- [Power Budget](05-Power-Budget/Power-Budget.md)

## Design Status

**Current Phase:** Preliminary Design / External Design Review

The subsystem architecture, component selections, schematic, and power budget are being developed and evaluated. Component specifications, power consumption, and system operation will be verified before final design approval.

