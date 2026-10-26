
# Bill of Materials — Microphone Subsystem

**EGR 304 | Team 203 | Joseph White**

**Status: Preliminary — October 26, 2026**

## Overview

This bill of materials (BOM) documents the components included in the microphone detection subsystem schematic.

The subsystem uses a microphone, an MCP6004 operational amplifier for analog signal conditioning, a PIC18F57Q43 Curiosity Nano development board, and an LM7805 regulator for the 5 V power rail.

The component list was exported from the current KiCad schematic. Quantities below represent schematic requirements and do not yet include prototyping components or replacement parts.

Manufacturer part numbers, prices, suppliers, and footprints will be verified before purchase requests are submitted.

## Bill of Materials

| Description | Qty | Reference | Manufacturer / Part Number | Unit Cost |
|---|---:|---|---|---|
| Capacitor, 0.33 µF, 25 V | 1 | C1 | TBD | TBD |
| Capacitor, 0.1 µF, 25 V | 5 | C2, C3, C4, C6, C7 | TBD | TBD |
| Capacitor, 0.22 µF, 25 V | 1 | C5 | TBD | TBD |
| Green LED | 1 | D2 | TBD | TBD |
| Red LED | 1 | D3 | TBD | TBD |
| Fuse, 1 A | 1 | F1 | TBD | TBD |
| DC barrel jack | 1 | J1 | TBD | TBD |
| 8-pin connector | 1 | J3 | TBD | TBD |
| Solder jumpers | 2 | JP1, JP2 | TBD | TBD |
| MEMS microphone, proposed | 1 | MK1 | 3SM121MZB1UA — verify | TBD |
| Resistor, 1 kΩ, ¼ W | 3 | R1, R5, R7 | TBD | TBD |
| Resistor, 10 kΩ, ¼ W | 5 | R3, R4, R13–R15 | TBD | TBD |
| Resistor, 2.2 kΩ, ¼ W | 1 | R6 | TBD | TBD |
| Resistor, 100 kΩ, ¼ W | 1 | R8 | TBD | TBD |
| Resistor, 220 Ω, ¼ W | 1 | R9 | TBD | TBD |
| Resistor, 330 Ω, ¼ W | 1 | R10 | TBD | TBD |
| Resistor, 100 Ω, ¼ W | 2 | R11, R12 | TBD | TBD |
| Momentary pushbutton | 1 | SW1 | TBD | TBD |
| Test points | 6 | TP1–TP6 | TBD | TBD |
| 5 V linear regulator | 1 | U1 | LM7805 — variant TBD | TBD |
| PIC18F57Q43 Curiosity Nano | 1 | U2 | Microchip — exact kit TBD | TBD |
| Quad operational amplifier, DIP-14 | 1 | U3 | Microchip MCP6004-I/P | TBD |

**Total: 39 schematic component instances across 23 grouped BOM entries.**

## Planned Design Revision

The proposed 3SM121MZB1UA microphone requires a compatible lower-voltage supply.

A dedicated 3.3 V regulator and any required supporting capacitors are planned additions. They are not included in the current schematic export or component totals.

The microphone power architecture must be verified and updated before PCB fabrication.

## Purchasing Requirements

Final order quantities will account for:

- Components required for the subsystem PCB.
- Breadboard-compatible components for prototyping.
- One or two additional parts per component instance where appropriate.
- Components already available in Peralta 109.

Purchase requests will be organized by vendor and submitted for instructor approval.

## Outstanding Items

- Confirm microphone electrical specifications and package.
- Add and verify the microphone supply regulator.
- Complete missing KiCad footprints.
- Verify manufacturer part numbers and datasheets.
- Determine stock availability and purchase quantities.
- Obtain vendor pricing and calculate total cost.
- Prepare vendor-specific purchase request spreadsheets.

## Design Status

**Preliminary BOM — pending component verification, schematic revisions, and purchasing approval.**
