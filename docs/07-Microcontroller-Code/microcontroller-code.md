# Microcontroller Code

## Microphone Subsystem

The microphone subsystem uses the PIC18F57Q43 Curiosity
Nano to read and process the amplified microphone signal.

## Software

- MPLAB X IDE
- XC8 Compiler
- MPLAB Code Configurator (MCC)

## Code Functionality

- Reads the amplified microphone signal using ADC on RA0.
- Converts the 12-bit ADC reading to an 8-bit DAC value.
- Outputs the analog signal through RA2.
- Transmits microphone readings through UART.
- Displays ADC and DAC readings in PuTTY.
- Controls the PCB red LED using the PCB pushbutton.
- Controls the onboard Nano LED using the onboard pushbutton.

## Hardware Verification

The subsystem hardware verification was demonstrated
in person with the instructor.

## Project Files

[Download Microcontroller Code (.zip)](Microphone_Lab.zip)
