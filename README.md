# Planetary Gear System
**Project Type:** Mechanical Design Demonstration

**Status:** Completed

**Date:** August 2026



## Table of Contents
- [Overview](#overview)
- [Design Approach](#design-approach)
  - [Parameters](#parameters)
- [How It Works](#how-it-works)
- [Assets](#assets)
  - [Images](#images)
  - [Demonstration](#demonstration)
- [Key Takeaways](#key-takeaways)



  
## Overview
A 3D CAD model of a planetary gear system designed and assembled in Autodesk Fusion 360.


## Design Approach

The planetary gear system was designed in Fusion 360 using a module of 2 mm and a pressure angle of 20°. The target configuration uses the ring gear as the fixed member, the sun gear as the input, and the planet carrier as the output, with a 6:1 speed reduction.

`R = Ring gear`
`S = Sun gear`
`P = Planet gear`
`Np = Number of planets`
`Gr = Gear ratio`



The ring gear was set to 80 teeth. The required sun gear teeth number was calculated from the gear ratio:

`S = R / ((1/Gr) - 1)`

`S = 80 / ((1/(1/6)) - 1)`

`S = 16 teeth`

The planet gear teeth number was determined from the relationship between the sun and ring gears:

`P = (R - S) / 2`

`P = (80 - 16) / 2`

`P = 32 teeth`

The three-planet arrangement was then cross-checked using:

`(R + S) / Np`

`(80 + 16) / 3 = 32`

The result is an integer which implies that the three planet gears can be evenly distributed around the sun gear while maintaining the required gear geometry.

The gears and planet carrier were modelled as separate components and assembled using appropriate joints to establish their relative positions and allow the required rotational movement.




### Parameters

| Parameter                        |                             Value |
| ---------------------------------|---------------------------------: |
| Module                           |                              2 mm |
| Pressure angle                   |                               20° |
| Sun gear teeth                   |                                16 |
| Planet gear teeth                |                                32 |
| Ring gear teeth                  |                                80 |
| Sun pitch diameter               |                             32 mm |
| Planet pitch diameter            |                             64 mm |
| Ring pitch diameter              |                            160 mm |
| Number of planet gears           |                                 3 |
| Planet gear spacing              |                              120° |
| Gear reduction                   |                               6:1 |
 

  
## How It Works
The ring gear is fixed while the sun gear provides the input rotation. The sun gear meshes with the three planet gears, causing them to rotate about their own axes. Since the planet gears are mounted on the carrier and also mesh with the fixed ring gear, their motion causes the carrier to rotate in the same direction as the sun gear at a slower speed. The selected gear tooth numbers give the system a 6:1 reduction. This means it takes six rotations of the sun gear for one full rotation of the carrier.



## Assets
### Images
#### Top View
![Top View](<Assets/Labelled View.png>)

#### Side View
![Side View](<Assets/Side View.png>)

#### Bottom View
![Bottom View](<Assets/Bottom View.png>)

### Demonstration
#### Preview
![Image](<Assets/Demo.gif>)

[Video](<Assets/Demonstration Video.mp4>)


## Key Takeaways
- The number of teeth and geometry of the sun, planet, and ring gears determine how the components mesh and interact in the planetary system.
- Joints define the allowed movement between components, providing the basis for accurately modelling the mechanism's motion.
- The interaction between constrained components can be used to reproduce the motion behaviours of  mechanical systems in a CAD environment.
- Planetary gear systems provide significant speed reduction and torque multiplication within a compact arrangement, making them useful in applications such as automotive transmissions and robotic actuators.
