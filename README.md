# USB dual voltage power supply
**Project Type:** PCB Design, Mechanical Design

**Status:** Complete, subject to modification.

**Date:** October 2026


## Table of Contents
- [Overview](#overview)
- [Components](#components)
- [Design Approach](#design-approach)
  - [PCB Design](#pcb-design)
  - [Case Design](#case-design)
- [How It Works](#how-it-works)
- [Assets](#assets)
  - [Images](#images)
- [Key Takeaways](#key-takeaways)


## Overview
The USB Dual-Voltage Power Supply is a compact power supply project designed to provide either 3.3V or 5V DC output from a USB power source designed in KiCAD. The casing was modelled in Fusion 360.

## Components
|Ref.|	Component	| Specification |	Footprint|
|--|-----|-----|-----|
|J1|	USB-C receptacle|	USB 2.0, 16 contacts, right-angle| connector_USB:USB_C_Receptacle_HRO_TYPE-C-31-M-12
|R1, R2|	CC resistors|	5.1 kΩ, 1%, 0.125 W	|Resistor_SMD:R_0805_2012Metric
|F1|	Resettable PTC fuse|	0.5 A hold current, ≥6 V rating, provisional|	Fuse:Fuse_1206_3216Metric
|U1|	3.3 V regulator|	AP2112K-3.3	|Package_TO_SOT_SMD:SOT-23-5
|C1|	Input capacitor|	1 µF, 16 V, X7R ceramic	|Capacitor_SMD:C_0805_2012Metric
|C2|	Output capacitor|	1 µF, 16 V, X7R ceramic	|Capacitor_SMD:C_0805_2012Metric
|C3|	Additional input capacitor|	10 µF, 16 V, X7R ceramic	|Capacitor_SMD:C_1206_3216Metric
|R3|	LED current-limiting resistor|1 kΩ, 0.125 W	|Resistor_SMD:R_0805_2012Metric
|D1|	Power indicator	Green LED| 2–3 V forward voltage|	LED_SMD:LED_0805_2012Metric
|J2|	Male output header|	1×3, 2.54 mm pitch, horizontal	|Connector_PinHeader_2.54mm:PinHeader_1x03_P2.54mm_Horizontal


## Design Approach
The PCB has a power input, voltage regulation circuitry and a three-pin output connector. The first pin supplies 3.3V, the second is the ground pin and the third is 5V. The project also incorporates a custom-designed enclosure to house and protect the PCB assembly.

### PCB Design
The PCB was designed in KiCad as a two-layer FR-4 board, measuring 48 × 16.5 mm with a thickness of 1.6 mm. It incorporates a USB-C power input, a resettable fuse for input protection, an AP2112K-3.3 voltage regulator, filtering capacitors and a power indicator LED. A three-pin header provides access to the 5 V and 3.3 V outputs, alongside a common ground connection.

| Parameter | Value (mm)|
|---|---|
| PCB Design Software | KiCad |
| Board Type | Two-layer FR-4 |
| Board Dimensions | 48 × 16.5 mm |
| Board Area | 792.4 mm² |
| Board Thickness | 1.6 mm |
| Minimum Track Width | 0.20 mm |
| Minimum Track Clearance | 0.21 mm |
| Minimum Drill Diameter | 0.30 mm |
| Front Copper Area | 129.0 mm² |
| Back Copper Area | 706.1 mm² |
| Front Footprint Area | 333.8 mm² |
| Back Footprint Area | 33.7 mm² |
| Front Footprint Density | 42.19% |
| Back Footprint Density | 4.26% |

The front copper layer accommodates the main component connections and power routing, while the back copper layer is primarily used as a ground plane. The board has a minimum track width of 0.20 mm, a minimum clearance of 0.21 mm and a minimum drill diameter of 0.30 mm.



### Case Design

| Parameter | Inches | Millimetres (mm) |
|---|---:|---:|
| **Full Case** | | |
| Length | 2.2 | 55.88 |
| Breadth | 1.0 | 25.40 |
| Height | 0.4 | 10.16 |
| **USB-C Outlet** | | |
| Length | 0.525 | 13.34 |
| Breadth | 0.300 | 7.62 |
| **Individual Case Half** | | |
| Length | 2.2 | 55.88 |
| Breadth | 1.0 | 25.40 |
| Height | 0.2 | 5.08 |
| **Design Software** | Autodesk Fusion 360 | |

## How It Works
The board receives a 5V DC supply through its USB-C receptacle. Two 5.1 kΩ pull-down resistors connected to the CC pins establish the USB-C sink configuration, allowing the power source to recognise the board as a power-consuming device and supply power.

The incoming supply passes through a resettable polyfuse, which provides overcurrent protection by increasing its resistance when excessive current causes it to heat up. An LED, connected through a current-limiting resistor, provides a visual indication that the board is powered.

The circuit provides two voltage outputs: 5V and 3.3V. The 5V output is supplied directly from the USB input through the polyfuse, while the AP2112K-3.3 low-dropout (LDO) regulator converts the incoming 5V supply to a regulated 3.3V output. This provides two selectable voltage levels for powering external devices.

Capacitors are incorporated into the circuit to support stable power delivery. They provide local charge storage, help suppress supply fluctuations and reduce electrical noise. The 1 µF, 16V capacitor is part of the regulator's supporting circuitry, helping maintain stable operation.



## Assets
### Images
#### Footprint View
![Top View](<Assets/Footprint View.png>)

#### Enclosed I View
![Top View](<Assets/Enclosed I View.png>)

#### Enclosed II View
![Top View](<Assets/Enclosed II View.png>)

#### Enclosed III View
![Top View](<Assets/Enclosed III View.png>)

#### Board View
![Top View](<Assets/Board View.png>)



## Key Takeaways
- The arrangement of components and copper tracks determines how electrical connections are distributed across a PCB, making component placement an important part of the design process.

- Copper zones provide a shared connection between components on the same electrical net, reducing the need for individually routed ground connections.

- Vias establish electrical connections between copper layers, allowing tracks to change layers and providing flexibility when routing a two-layer PCB.

- Decoupling capacitors help maintain stable supply voltages by responding to transient current demands and reducing electrical noise.

- Component footprints determine the physical arrangement of solder pads and must correspond to the dimensions and pin configurations of the selected components.

- PCB dimensions, component heights and connector positions must be considered together when designing an enclosure to ensure proper fit and accessibility.

- Creating a specific layer specifically for the ground connection is effective for simplifying copper traces on the board.
