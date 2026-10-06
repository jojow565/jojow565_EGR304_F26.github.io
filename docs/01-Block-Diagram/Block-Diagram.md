---
title: Block Diagram
tags:
- block diagram
- microphone
---

## Overview

This block diagram shows the major components and signal connections for the Team 203 microphone board. The MEMS microphone produces an analog signal that is conditioned by the MCP6004 op amp before being sent to the ADC input of the Microchip PIC18F57Q43 Curiosity Nano.

The microcontroller provides the digital I/O connections for the push button, red LED, and the 8-pin ribbon cable connector used to interface with the other team boards. The board uses a 5V 1.5A voltage regulator, with the system powered from the 9V 3A unregulated power supply.

## Block Diagram

![Team 203 Microphone Board Block Diagram](Team%20304.drawio.png)
