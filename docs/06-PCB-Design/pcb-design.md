---
title: PCB Design
tags:
- PCB
- KiCad
- microphone
---

# PCB Design — Microphone Subsystem

**EGR 304 | Team 203 | Joseph White**

**Updated: November 25, 2026**

## Overview

This page documents the printed circuit board (PCB) designed, manufactured, assembled, and tested for the microphone subsystem developed as part of the EGR 304 Embedded Systems team project.

The PCB was designed using KiCad and consists of two copper layers. The design includes the power regulation circuit, microphone signal-conditioning circuit, microcontroller connections, debugging components, test points, and team communication interface.

## PCB Layout

The following images show the top and bottom copper layers of the PCB design.

### Top Copper Layer

![Top PCB Layout](EGR304_JW_PCB_Top.png)

**Figure 1:** Top copper layer showing routed electrical connections, component pads, and copper features.

### Bottom Copper Layer

![Bottom PCB Layout](EGR304_JW_PCB_Bottom.png)

**Figure 2:** Bottom copper layer showing additional routed connections and the ground copper plane.

## PCB Specifications

| Specification | Description |
|---|---|
| Project | Microphone Subsystem |
| Course | EGR 304 – Embedded Systems |
| Designer | Joseph White |
| Team | 203 |
| PCB Design Software | KiCad |
| Board Material | FR-4 |
| Copper Layers | 2 |
| Board Thickness | 1.6 mm |
| Copper Thickness | 1 oz |
| Soldermask Color | Green |
| Assembly Method | Manual soldering |
| External Power Supply | 9 V DC |
| Regulated Supply | 5 V DC |
| Microcontroller | PIC18F57Q43 Curiosity Nano |
| Team Interface | 8-pin connector |

## PCB Circuit Sections

The PCB contains the following functional circuit sections:

### Power Regulation

- DC barrel jack input.
- 1 A fast-acting fuse.
- STMicroelectronics L7805ABV voltage regulator.
- Input and output bypass capacitors.
- Green power indicator LED.

### Microphone Signal Conditioning

- Two-wire electret condenser microphone.
- Microchip MCP6004-I/P operational amplifier.
- Adjustable 10 kΩ potentiometer.
- Reference voltage divider.
- AC coupling capacitor.
- RC low-pass filter.

### Microcontroller

- Microchip PIC18F57Q43 Curiosity Nano.
- RA0 microphone ADC input.
- RA2 DAC output.
- Digital input and output connections.
- UART communication interface.

### Debugging and Testing

- Momentary pushbutton.
- Red indicator LED.
- Six test points.
- Eight-pin team connector.
- PCB solder jumpers.

## PCB Design Files

The following files contain the PCB layout documentation, KiCad project, and manufacturing files.

### PCB Layout PDF

The PDF contains the top and bottom copper layer layouts for detailed viewing and printing.

[Download Top and Bottom PCB Layout (PDF)](Team203_PCB_top%20and%20bottom.pdf)

### KiCad Project Files

The KiCad project archive contains the schematic, PCB layout, project configuration files, and custom footprint libraries.

[Download Complete KiCad Project (ZIP)](EGR304_JW_Team203_KiCad.zip)

### Gerber Manufacturing Files

The Gerber archive contains the manufacturing files required for PCB fabrication, including:

- Top and bottom copper layers.
- Board outline.
- Soldermask layers.
- Silkscreen layers.
- Drill files.

[Download Gerber Manufacturing Files (ZIP)](EGR304_JW_Team203%20%282%29.zip)

## Design Verification

The PCB design was checked using KiCad's Design Rules Checker (DRC).

The Gerber and drill files were generated and uploaded to the JLCDFM online manufacturing analysis tool.

The manufacturing analysis reported zero Danger findings.

The PCB was subsequently manufactured and assembled for individual subsystem hardware verification.

## PCB Assembly

The microphone subsystem PCB was manually assembled using the selected through-hole components, connectors, and microcontroller development board.

The assembled subsystem includes the regulated power supply, microphone amplifier circuit, pushbutton, indicator LEDs, and communication connections.

During hardware troubleshooting, incorrectly installed capacitors were identified and corrected.

The subsystem was subsequently demonstrated to the instructor during individual hardware verification.

## Hardware Verification

Individual subsystem hardware verification was demonstrated to the instructor on November 25, 2026.

The microcontroller verification firmware was developed using MPLAB X IDE, XC8, and MPLAB Code Configurator (MCC).

The firmware provides:

- Microphone signal acquisition through the ADC.
- Analog signal reproduction through the DAC.
- UART transmission.
- PuTTY serial debugging.
- PCB pushbutton and LED control.
- Curiosity Nano pushbutton and LED control.

The verification firmware and complete MPLAB X project are available on the Microcontroller Code page.

[View Microcontroller Code](../07-Microcontroller-Code/microcontroller-code.md)

## Design Status

| Development Stage | Status |
|---|---|
| Schematic Design | Complete |
| PCB Layout | Complete |
| Design Rules Check | Performed |
| Manufacturing Analysis | Performed |
| PCB Manufacturing | Complete |
| Component Assembly | Complete |
| Firmware Development for Verification | Complete |
| Individual Hardware Verification | Complete |
| Final Team Communication | In Development |
| Final Team Integration | In Development |

## Conclusion

The microphone subsystem PCB has progressed from preliminary design through manufacturing, assembly, firmware development, and individual hardware verification.

The PCB layout images, PDF documentation, KiCad project archive, and Gerber manufacturing files are provided above.

Final team communication and subsystem integration remain the next stages of project development.

---

## Related Documentation

- [Block Diagram](../01-Block-Diagram/Block-Diagram.md)
- [Component Selection](../02-Component-Selection/Component-Selection.md)
- [Bill of Materials](../03-BOM/BOM.md)
- [Electrical Schematic](../04-Schematic/schematic.md)
- [Power Budget](../05-Power-Budget/Power-Budget.md)
- [Microcontroller Code](../07-Microcontroller-Code/microcontroller-code.md)
