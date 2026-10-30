---
title: Bill of Materials
---

# Bill of Materials

**Name:** Sam Kholmuminov<br>
**Team:** Team 102 – Project Aurora<br>
**Subsystem:** Storage Environment (Board D: Temperature & Light)<br>
**Schematic revision:** 3 (40 reference designators)<br>
**Prices and stock checked:** October 30, 2026 (Digi-Key)<br>
**Last updated:** October 30, 2026

## What this page is

This page lists every part on my **Storage Environment board**, where each one comes from, and what it costs. The list comes straight from the Rev 3 KiCad schematic on my [Schematics](../04-Schematic/schematic.md) page (all 40 reference designators), plus the things the schematic does not show as separate symbols: the fuse clips that hold F1, the shunts that go on JP1 and JP2, the female headers the Curiosity Nano plugs into, and the wall adapter that plugs into J2.

The parts fall into three groups:

* **Buy from Digi-Key** – the sensors, the op-amp, the regulator, the ribbon-cable header, the fuse clips and the jumper shunts. These are the only parts that cost money from my $60 budget.
* **Peralta 109 general stock** – the 500 mA fuse and the 14-pin DIP socket. The lab keeps both in stock, so I do not need to order them.
* **Already on hand** – the Curiosity Nano (issued by the course), the wall adapter, the barrel jack, resistors, capacitors, LEDs, headers and the pushbutton, which I have from the course supply kit and my own stock.

## Downloads

| File | What it is |
|:--|:--|
| [Storage_Environment_Board_SK_BOM.xlsx](files/Storage_Environment_Board_SK_BOM.xlsx) | The same BOM as a spreadsheet, in the layout of the course BOM example, with the order quantities and totals as formulas |
| [Purchase_Request_DigiKey_SK.pdf](files/Purchase_Request_DigiKey_SK.pdf) | PDF copy of the Digi-Key purchase request I sent to my professor (one vendor, one form) |

## Summary

*Table 1: Where the parts come from and what they cost me*

| Group | Lines in the BOM | Cost to my budget |
|:--|:--:|--:|
| Buy from Digi-Key (Table 2) | 7 | $24.24 for 40 pieces (board set + breadboard set + spares) |
| Peralta 109 general stock (Table 3) | 2 | $0.00 |
| Already on hand (Table 4) | 21 | $0.00 |
| Digi-Key shipping (USPS Ground Advantage) | – | $4.99 |
| **Estimated total** | | **$29.23** |
| **Budget** | | $60.00 |
| **Left for changes and mistakes** | | **$30.77** |

Digi-Key notes on its product pages that a tariff may be added at checkout for some parts; if that happens the business office will see it in the cart. Even if it added a few dollars, the order stays far below the budget.

## Parts to buy (Digi-Key)

*Table 2: Purchase list. "Qty on board" is how many one board uses; "Order qty" is what is on the purchase request.*

| Ref | Part | Qty on board | Order qty | Manufacturer | Manufacturer # | Digi-Key # (link) | Unit price | Line total | Datasheet |
|:--|:--|:--:|:--:|:--|:--|:--|--:|--:|:--|
| R2 | CdS photocell (light-dependent resistor), 550 nm peak, 20–100 kΩ at 10 lux, 5 mm radial | 1 | **4** | Advanced Photonix | NSL-19M51 | [NSL-19M51-ND](https://www.digikey.com/en/products/detail/advanced-photonix/NSL-19M51/5039794) | $1.10 | $4.40 | [Datasheet (PDF)](datasheets/NSL-19M51_photocell_datasheet.pdf) |
| RT1 | NTC thermistor 10 kΩ ±5 %, B = 4300 K, leaded disc | 1 | **4** | TDK (EPCOS) | B57164K0103J000 | [495-2080-ND](https://www.digikey.com/en/products/detail/tdk/B57164K0103J000/739847) | $0.57 | $2.28 | [Datasheet (PDF)](datasheets/TDK_B57164K_NTC_thermistor_datasheet.pdf) |
| U3 | Quad rail-to-rail op-amp, 1 MHz, single supply 1.8–6 V, 14-pin DIP | 1 | **4** | Microchip Technology | MCP6004-I/P | [MCP6004-I/P-ND](https://www.digikey.com/en/products/detail/microchip-technology/MCP6004-I-P/523060) | $0.60 | $2.40 | [Datasheet (PDF)](datasheets/MCP6004_op-amp_datasheet.pdf) |
| U2 | 5 V positive linear voltage regulator, 1.5 A, TO-220 | 1 | **4** | STMicroelectronics | L7805CV | [497-1443-5-ND](https://www.digikey.com/en/products/detail/stmicroelectronics/L7805CV/585964) | $1.14 | $4.56 | [Datasheet (PDF)](datasheets/L7805CV_L78_regulator_datasheet.pdf) |
| F1 (holder) | Fuse clip for 5 × 20 mm cartridge fuse, PCB mount, 15 A (2 clips per fuse) | 2 | **10** | Keystone Electronics | 3517 | [36-3517-ND](https://www.digikey.com/en/products/detail/keystone-electronics/3517/316010) | $0.287 | $2.87 | [Datasheet (PDF)](datasheets/Keystone_3517_fuse_clip_datasheet.pdf) |
| J1 | 2 × 4 shrouded box header, 2.54 mm, vertical, through-hole (team ribbon cable) | 1 | **4** | Molex | 0702460801 | [23-0702460801-ND](https://www.digikey.com/en/products/detail/molex/0702460801/760165) | $1.86 | $7.44 | [Datasheet (PDF)](datasheets/Molex_0702460801_box_header_drawing.pdf) |
| JP1, JP2 (shunts) | Jumper shunt, 2 position, 2.54 mm, closed top, black | 2 | **10** | Sullins Connector Solutions | SPC02SYAN | [S9001-ND](https://www.digikey.com/en/products/detail/sullins-connector-solutions/SPC02SYAN/76375) | $0.029 | $0.29 | [Datasheet (PDF)](datasheets/Sullins_SPC02SYAN_shunt_drawing.pdf) |
| **Total** | | | **40 pieces** | | | | | **$24.24** | |

The unit prices are Digi-Key's prices on October 30, 2026 for the quantity I am ordering. The fuse clips and the shunts hit a price break at 10 pieces, so 10 of each is cheaper than 8 (clips: 10 for $2.87 instead of 8 for $3.04; shunts: 10 for $0.29 instead of 8 for $0.80).

## Parts from Peralta 109

*Table 3: Parts I take from the lab's general stock instead of ordering*

| Ref | Part | Qty on board | Manufacturer | Part # | Where it is | Datasheet |
|:--|:--|:--:|:--|:--|:--|:--|
| F1 (fuse) | Fuse, 5 × 20 mm glass cartridge, 500 mA fast-acting, 250 V | 1 | Littelfuse / NTE (lab stock) | 217 series (0217.500) or equivalent | Peralta 109 keeps 500 mA 5 × 20 mm fuses in general stock | [Datasheet](https://www.littelfuse.com/products/fuses/cartridge-fuses/5x20mm-fuses/217) |
| U3 (socket) | IC socket, 14-pin DIP, 7.62 mm (0.3 in) row spacing | 1 | generic (lab stock) | 14-pin DIP socket | Peralta 109 keeps 8/14/16/40-pin DIP sockets in the parts closet | n/a (generic lab part) |

## Parts already on hand

*Table 4: Parts from the course supply kit and my own stock ($0 from the budget)*

| Ref | Part | Qty on board | Manufacturer | Part # | Where it comes from | Datasheet |
|:--|:--|:--:|:--|:--|:--|:--|
| U1 | PIC18F57Q43 Curiosity Nano evaluation board (course-issued microcontroller board) | 1 | Microchip Technology | DM164150 | Issued by the course; does not count against the budget | [Datasheet](https://ww1.microchip.com/downloads/en/DeviceDoc/PIC18F57Q43-Curiosity-Nano-HW-UserG-DS40002186A.pdf) |
| U1 (socket) | Female header 1 × 28, 2.54 mm (two rows, cut from 1 × 40 strips) to socket the Curiosity Nano on the PCB | 2 | generic | 1×40 female header strip | From my header stock; Peralta also has 1 × 40 female strips | n/a |
| R1 | Resistor 1 kΩ, 1/4 W, 5 %, axial (power LED) | 1 | generic | — | Resistor kit | n/a |
| R3 | Resistor 3.3 kΩ, 1/4 W, 5 %, axial (photocell divider) | 1 | generic | — | Resistor kit | n/a |
| R4, R6, R8, R12 | Resistor 10 kΩ, 1/4 W, 5 %, axial (gain stage, filters, button pull-up) | 4 | generic | — | Resistor kit | n/a |
| R7 | Resistor 10 kΩ, 1/4 W, 1 %, axial (thermistor divider; 1 % keeps the temperature error small) | 1 | generic | — | Resistor kit (use a 1 % part if the kit has one; otherwise measure and note the real value) | n/a |
| R5 | Resistor 33 kΩ, 1/4 W, 5 %, axial (gain-stage feedback) | 1 | generic | — | Resistor kit | n/a |
| R9 | Resistor 100 Ω, 1/4 W, 5 %, axial (DAC output protection) | 1 | generic | — | Resistor kit | n/a |
| R10, R11 | Resistor 330 Ω, 1/4 W, 5 %, axial (LED current limit) | 2 | generic | — | Resistor kit | n/a |
| C1 | Ceramic capacitor 0.33 µF, 50 V, 5 mm pitch (regulator input) | 1 | generic | — | Capacitor kit | n/a |
| C2, C4, C5, C6, C8 | Ceramic capacitor 0.1 µF, 50 V, 5 mm pitch (bypass, filter, debounce) | 5 | generic | — | Capacitor kit; Peralta 109 also stocks 0.1 µF 50 V | n/a |
| C3 | Electrolytic capacitor 10 µF, 25 V, radial 5 mm (input bulk) | 1 | generic | — | Capacitor kit | n/a |
| C7 | Ceramic capacitor 1 µF, 50 V, 5 mm pitch (temperature filter) | 1 | generic | — | Capacitor kit | n/a |
| D1, D2, D3 | LED 5 mm: green (power), red (warning), yellow (debug/heartbeat) | 3 | generic | — | Course supply kit | n/a |
| J2 | DC barrel jack 2.1 × 5.5 mm, right angle, through-hole (9–12 V input) | 1 | CUI Devices | PJ-102A / PJ-102AH | Course supply kit; Peralta 109 also stocks PJ-102AH | [Datasheet](https://www.cuidevices.com/product/resource/pj-102a.pdf) |
| J3 | Pin header 1 × 10, 2.54 mm, male, vertical (spare GPIO), cut from 1 × 40 strip | 1 | generic | 1×40 male header strip | Header stock | n/a |
| J4 | Pin header 1 × 8, 2.54 mm, male, vertical (power / analog spare), cut from 1 × 40 strip | 1 | generic | 1×40 male header strip | Header stock | n/a |
| JP1, JP2 (headers) | Pin header 1 × 2, 2.54 mm, male, vertical (isolation jumpers), cut from 1 × 40 strip | 2 | generic | 1×40 male header strip | Header stock | n/a |
| SW1 | Tactile pushbutton switch, 6 × 6 mm, through-hole (debug button) | 1 | generic | — | Course supply kit | n/a |
| TP1–TP5 | Test point: plated through-hole pad 1.5 mm; fitted with a cut-off header pin or wire loop | 5 | — | — | Part of the PCB; the pin comes from the header strip | n/a |
| (off board) | Wall adapter 9 V, 670 mA, regulated, 2.1 × 5.5 mm center-positive plug | 1 | Bel Power Solutions (CUI) | SWI6-9-N-P5 | Course supply kit; powers the board through J2 | [Datasheet](https://belfuse.com/media/datasheets/products/power-supplies/SWI6-N.pdf) |

All resistors are 1/4 W; the ceramic capacitors are 50 V parts and the electrolytic is 25 V, which is more than double the 12 V it can ever see (see the ratings note on the schematic).

## Why these quantities

The assignment says to order one of each part for a breadboard prototype, one for the PCB, and one or two extra in case something gets damaged. I followed that:

* **4 of each main part** (photocell, thermistor, MCP6004, L7805, Molex header): 1 for the breadboard, 1 for the PCB and 2 spares. The sensors are the parts most likely to be bent, overheated or lost, so two spares is cheap insurance.
* **10 fuse clips** (2 per board) and **10 shunts** (2 per board): 10 is the first price break on both, and it costs less than ordering 8.
* **Fuse and DIP socket from Peralta 109**: the lab has a selection of 5 × 20 mm fuses and 14-pin DIP sockets, so ordering them would only add cost and shipping weight.
* **Everything else on hand**: resistors, capacitors, LEDs, headers, the pushbutton, the barrel jack and the wall adapter came with the course supply kit or are in my parts box, so I am not ordering them. If one of the less common values (3.3 kΩ, 33 kΩ, 100 Ω, 0.33 µF, 1 µF, 10 µF) turns out to be missing, it is a cheap add-on to a later order and the $30 left in the budget covers it.

Headers come from 1 × 40 strips: the 1 × 10, 1 × 8 and 1 × 2 male headers and the two 1 × 28 female headers for the Nano are snapped or cut to length. All of them are 2.54 mm (0.1 in) pitch, the same as a breadboard.

## Debugging, expansion and error-proofing hardware

The assignment asks for hardware that makes the board easy to test and hard to damage. Table 5 shows where each item is on my board.

*Table 5: Checklist from the Hardware Orders assignment*

| Item | On my board | How it is sourced |
|:--|:--|:--|
| Test points | TP1 (VIN), TP2 (+5V), TP3 (Earth), TP4 (LIGHT_ADC), TP5 (TEMP_ADC) | Plated pads on the PCB with a header pin pressed in (on hand) |
| Jumpers | JP1 (+5V → VTG) and JP2 (VOFF → Earth) isolate the Nano's power | 1 × 2 headers on hand; shunts ordered (Sullins SPC02SYAN) |
| Male / female headers | J3 1 × 10 spare GPIO, J4 1 × 8 power / analog spare; two 1 × 28 female headers socket the Nano | Cut from 1 × 40 strips (on hand) |
| PCB-mount connectors, sockets, plugs | J1 Molex 2 × 4 box header (team ribbon cable), J2 CUI PJ-102A barrel jack | Molex header ordered; barrel jack on hand |
| Fuses and fuse holders | F1 500 mA fast-acting 5 × 20 mm fuse in two Keystone 3517 clips | Clips ordered; fuse from Peralta 109 |
| IC sockets | 14-pin DIP socket under U3 (MCP6004), so the op-amp can be swapped without desoldering | Peralta 109 parts closet |

## Order status

* **Vendor:** everything comes from Digi-Key, so there is one purchase request (course template, one vendor per form). It has 7 lines, so no shopping-cart link is needed (that is only required above 10 lines).
* **Sent to:** Zane Reynolds (10:30 AM section) for approval on October 30, 2026. The business office needs about five business days to place and receive the order, so I sent it as soon as the BOM was done.
* **Stock:** every part was in stock at Digi-Key on October 30, 2026 (Table 6), so nothing is on back order and the order should ship the same day it is placed.

*Table 6: Digi-Key stock on October 30, 2026*

| Part | Digi-Key stock (October 30, 2026) | I am ordering |
|:--|:--|:--:|
| NSL-19M51 | 11,468 in stock | 4 |
| B57164K0103J000 | 16,765 in stock | 4 |
| MCP6004-I/P | 2,278 in stock | 4 |
| L7805CV | 85,358 in stock | 4 |
| 3517 | 129,838 in stock | 10 |
| 0702460801 | 1,746 in stock | 4 |
| SPC02SYAN | 1,458,857 in stock | 10 |

## Datasheets

The datasheet of every part I am buying is saved in this repository (folder `docs/03-BOM/datasheets/`), so the links keep working even if a manufacturer moves its files. Table 7 lists the copies and where they came from.

*Table 7: Datasheets stored in the repository*

| Part | Used as | Copy in this repository | Where it came from |
|:--|:--|:--|:--|
| Advanced Photonix NSL-19M51 | CdS photocell (light sensor) | [NSL-19M51_photocell_datasheet.pdf](datasheets/NSL-19M51_photocell_datasheet.pdf) | [source](https://mm.digikey.com/Volume0/opasdata/d220001/medias/docus/6165/nsl-19m51.pdf) |
| TDK (EPCOS) B57164K0103J000 | 10 kΩ NTC thermistor (temperature sensor) | [TDK_B57164K_NTC_thermistor_datasheet.pdf](datasheets/TDK_B57164K_NTC_thermistor_datasheet.pdf) | [source](https://www.tdk-electronics.tdk.com/inf/50/db/ntc/NTC_Leaded_disks_K164.pdf) |
| Microchip Technology MCP6004-I/P | Quad op-amp MCP6004, 14-pin DIP | [MCP6004_op-amp_datasheet.pdf](datasheets/MCP6004_op-amp_datasheet.pdf) | [source](https://ww1.microchip.com/downloads/en/DeviceDoc/MCP6001-1R-1U-2-4-1-MHz-Low-Power-Op-Amp-DS20001733L.pdf) |
| STMicroelectronics L7805CV | 5 V linear regulator L7805CV, TO-220 | [L7805CV_L78_regulator_datasheet.pdf](datasheets/L7805CV_L78_regulator_datasheet.pdf) | [source](https://www.st.com/resource/en/datasheet/l78.pdf) |
| Keystone Electronics 3517 | Fuse clips for 5 × 20 mm fuse (2 per fuse) | [Keystone_3517_fuse_clip_datasheet.pdf](datasheets/Keystone_3517_fuse_clip_datasheet.pdf) | [source](https://www.keyelco.com/userAssets/file/K75p52.pdf) |
| Molex 0702460801 | 2×4 shrouded box header for the team ribbon cable | [Molex_0702460801_box_header_drawing.pdf](datasheets/Molex_0702460801_box_header_drawing.pdf) | [source](https://www.molex.com/en-us/products/part-detail/702460801?display=pdf) |
| Sullins Connector Solutions SPC02SYAN | Jumper shunts for the isolation jumpers | [Sullins_SPC02SYAN_shunt_drawing.pdf](datasheets/Sullins_SPC02SYAN_shunt_drawing.pdf) | [source](https://drawings-pdf.s3.amazonaws.com/11134.pdf) |

The parts I already own or take from the lab link to the manufacturer's page:

* [Littelfuse / NTE 217 series (0217.500)](https://www.littelfuse.com/products/fuses/cartridge-fuses/5x20mm-fuses/217) — Fuse, 5 × 20 mm glass cartridge, 500 mA fast-acting, 250 V
* [Microchip Technology DM164150](https://ww1.microchip.com/downloads/en/DeviceDoc/PIC18F57Q43-Curiosity-Nano-HW-UserG-DS40002186A.pdf) — PIC18F57Q43 Curiosity Nano evaluation board
* [CUI Devices PJ-102A / PJ-102AH](https://www.cuidevices.com/product/resource/pj-102a.pdf) — DC barrel jack 2.1 × 5.5 mm, right angle, through-hole
* [Bel Power Solutions (CUI) SWI6-9-N-P5](https://belfuse.com/media/datasheets/products/power-supplies/SWI6-N.pdf) — Wall adapter 9 V, 670 mA, regulated, 2.1 × 5.5 mm center-positive plug

Resistors, capacitors, LEDs, generic headers, the tactile switch and the DIP socket are generic kit or lab parts with no single manufacturer datasheet; their ratings (1/4 W, 50 V, 25 V, 5 mm LEDs, 6 mm switch) are on the schematic.

## Sources I used

* [Individual – Hardware Orders assignment](https://embedded-systems-design.bitbucket.io/304/individual-assignments/bom-and-hardware-orders/), the course [Bill of Materials template page](https://embedded-systems-design.github.io/EGR304DataSheetTemplate/03-BOM/BOM/), the Bill of Materials example spreadsheet and the Class Order Form (purchase request) template
* The course's Peralta 109 stock list (Spring 2023 Order Planning spreadsheet): fuses, DIP sockets, headers, 0.1 µF capacitors and PJ-102AH jacks in general stock
* [Sources for Electrical and Electromechanical Components](https://embedded-systems-design.github.io/sources-for-electrical-and-electromechanical-components/) on the Embedded Systems Design blog
* Digi-Key product pages linked in Table 2 (prices and stock on October 30, 2026) and the [Digi-Key delivery time and cost page](https://www.digikey.com/en/help-support/delivery-information/delivery-time-and-cost) (USPS Ground Advantage $4.99)
* My [Component Selection](../02-Component-Selection/Component-Selection.md) (why each part was chosen) and [Schematics](../04-Schematic/schematic.md) (the 40 reference designators) pages
