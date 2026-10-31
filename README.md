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
The USB Dual-Voltage Power Supply is a compact power supply project designed to provide either 3.3V or 5V DC output from a USB power source.

## Components
|Ref.|	Component	| Specification |	Footprint|
|--|-----|-----|-----|
|J1	USB-C receptacle	USB 2.0, 16 contacts, right-angle connector_USB:USB_C_Receptacle_HRO_TYPE-C-31-M-12
|R1, R2|	CC resistors	5.1 kΩ, 1%, 0.125 W	Resistor_SMD:R_0805_2012Metric
|F1|	Resettable PTC fuse	0.5 A hold current, ≥6 V rating, provisional	Fuse:Fuse_1206_3216Metric
|U1|	3.3 V regulator	AP2112K-3.3	Package_TO_SOT_SMD:SOT-23-5
|C1|	Input capacitor	1 µF, 16 V, X7R ceramic	Capacitor_SMD:C_0805_2012Metric
|C2|	Output capacitor	1 µF, 16 V, X7R ceramic	Capacitor_SMD:C_0805_2012Metric
|C3|	Additional input capacitor	10 µF, 16 V, X7R ceramic	Capacitor_SMD:C_1206_3216Metric
|R3|	LED current-limiting resistor	1 kΩ, 0.125 W	Resistor_SMD:R_0805_2012Metric
|D1|	Power indicator	Green LED, approximately 2–3 V forward voltage	LED_SMD:LED_0805_2012Metric
|J2|	Male output header	1×3, 2.54 mm pitch, vertical	Connector_PinHeader_2.54mm:PinHeader_1x03_P2.54mm_Vertical


## Design Approach
The PCB has a power input, voltage regulation circuitry and a three-pin output connector. The first pin supplies 3.3V, the second is the ground pin and the third is 5V. The project also incorporates a custom-designed enclosure to house and protect the PCB assembly.

  
## How It Works




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

