---
title: Power Budget
---

# Power Budget

**Name:** Sam Kholmuminov<br>
**Team:** Team 102 – Project Aurora<br>
**Subsystem:** Storage Environment (Board D: Temperature & Light)<br>
**Status:** Draft for the initial Component Selection submission. The course says the power budget is optional for the first submission but required for the external design review, so the numbers below will be moved into the course Excel template (and the finished sheet pasted here as images) before the design review.

## Overview

The power budget checks one simple thing: can my power source and my regulator supply every part on the board at the same time, with a 25 % safety margin? My board has one power rail (5 V) fed by one linear regulator (L7805CV) from one external source (9 V wall adapter). The parts and the reasons for choosing them are on the [Component Selection](../02-Component-Selection/Component-Selection.md) page.

## Section A – Parts that use power (worst-case current)

| Part | Rail | Max current | Where the number comes from |
|:--|:--|:--|:--|
| PIC18F57Q43 Curiosity Nano (PIC at 64 MHz, debugger off when no USB) | 5 V | 25 mA | PIC18F57Q43 datasheet run current plus margin |
| MCP6004-I/P quad op-amp | 5 V | 0.4 mA | 100 µA per amplifier × 4 (datasheet) |
| Red warning LED (RC5) | 5 V | 10 mA | 330 Ω series resistor on 5 V |
| Debug LED | 5 V | 10 mA | 330 Ω series resistor on 5 V |
| Heartbeat / spare LED | 5 V | 10 mA | 330 Ω series resistor on 5 V |
| Photocell divider (NSL-19M51 + 3.3 kΩ) | 5 V | 1.5 mA | 5 V ÷ 3.3 kΩ worst case (photocell near 0 Ω in bright light) |
| Thermistor divider (10 kΩ NTC + 10 kΩ) | 5 V | 0.5 mA | 5 V ÷ 10 kΩ worst case |
| Vref divider for the gain stage (10 kΩ + 10 kΩ) | 5 V | 0.25 mA | 5 V ÷ 20 kΩ |
| Pull-up resistor on the debug button (10 kΩ) | 5 V | 0.5 mA | only while the button is pressed |
| **Total on the 5 V rail** | | **about 58 mA** | |

## Section B – Rails

| Rail | Parts | Current needed | With 25 % safety margin |
|:--|:--|:--|:--|
| 5 V (logic + sensors) | everything above | 58 mA | **73 mA** |

The board has only one rail, which keeps the design simple and matches the course requirement for a single 5 V linear regulator.

## Section C – Regulator

| Rail | Regulator chosen | Max output current | Input needed | Heat at 73 mA |
|:--|:--|:--|:--|:--|
| 5 V | L7805CV (STMicroelectronics, TO-220) | 1.5 A | 7 V to 35 V | (9 V − 5 V) × 0.073 A = 0.29 W → no heat sink needed |

Why the L7805CV and not the alternatives is explained in Table 4 on the Component Selection page.

## Section D – External power source

| Source | Output | Can supply | Regulators connected | Remaining current |
|:--|:--|:--|:--|:--|
| SWI6-9-N-P5 9 V regulated wall adapter | 9 V DC | 670 mA | L7805CV (draws 73 mA + 8 mA quiescent = 81 mA) | 670 − 81 = **589 mA left (positive, OK)** |

## Section E – Battery life

Not applicable: the board runs from a wall adapter. For comparison, a 9 V alkaline battery (about 480 mAh) would last only 480 mAh ÷ 81 mA ≈ 6 hours, which is one reason a battery was rejected.

## Conclusions

One 5 V rail, about 58 mA worst case (73 mA with margin), a regulator rated for 1.5 A and an adapter rated for 670 mA: the supply has more than eight times the current the board needs, and the regulator stays cool without a heat sink.

## Resources

The course power budget template is available as a PDF [here](PowerBudgetExample.pdf) and as an Excel sheet [here](PowerBudgetExample.xlsx). The completed template will replace the tables above before the design review.
