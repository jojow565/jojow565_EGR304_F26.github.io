---
title: Block Diagram
tags:
- block diagram
- microphone
---



## Overview

This block diagram illustrates the major components and signal connections for the Team 203 microphone detection subsystem.

The microphone converts acoustic signals into electrical signals. These signals are conditioned by an MCP6004 operational amplifier circuit before being sent to an analog-to-digital converter (ADC) input on the Microchip PIC18F57Q43 Curiosity Nano development board.

The microcontroller provides digital input/output connections for the pushbutton, indicator LED, and interface connections to other team subsystems.

The proposed power architecture uses an external 9–12 V DC supply and an LM7805 linear voltage regulator to provide a regulated 5 V rail.

The microphone type and final external power supply specifications are pending verification.


## Block Diagram

![Team 203 Microphone Board Block Diagram](Team%20304.drawio.png)
