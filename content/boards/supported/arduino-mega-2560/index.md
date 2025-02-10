---
title: Arduino Mega 2560 Rev3
description: Details on MobiFlight support for the Arduino Mega 2560 Rev3.
ogimage: card-images/boards/mega-2560-rev3.png
weight: 10
---

The Arduino Mega 2560 Rev3 is a classic Arduino board with 70 IO pins and a relatively low cost.
While it has historically been a popular board for MobiFlight projects, the newer [Mega 2560 Pro Mini](/boards/mega-2560-pro-mini) is a better option for new projects.

{{< cards >}}

{{< card title="Arduino Mega 2560 Rev3" subtitle="ATmega2560 microcontroller" image="card-images/boards/mega-2560-rev3.png" >}}

{{</ cards >}}

> [!WARNING]
> Many lower-cost Mega 2560 Rev3 boards, particularly those purchased from AliExpress, use the CH340G chip for serial communication to the PC. These chips are frequently counterfeit and require [additional driver installation](/guides/installing-drivers/).

## Specifications

- 54 digital IO pins, 15 with PWM support.
- 16 analog inputs (can be used as digital inputs).

| Device                                                   | Limit | Notes                                                                                                                                    |
| -------------------------------------------------------- | :---: | ---------------------------------------------------------------------------------------------------------------------------------------- |
| [Analog input](/devices/potentiometer/)                  |  16   |                                                                                                                                          |
| [Button](/devices/button-switch/)                        |  68   |                                                                                                                                          |
| [Digital Input Multiplexer](/devices/multiplexer/)       |   6   |                                                                                                                                          |
| [Encoder](/devices/encoder/)                             |  20   |                                                                                                                                          |
| [Input shift register](/devices/input-shift-register/)   |   6   | Six _chains_ of shift registers, 32 bits each (2x16 or 4x8 bit shift registers).                                                         |
| [LCD Display](/devices/lcd/)                             |   2   |                                                                                                                                          |
| [LED / Output](/devices/led/)                            |  68   |                                                                                                                                          |
| [LED 7-Segment](/devices/seven-segment-display/)         |   6   | 6 TM1637 modules, or 6 chains of MAX7219 modules, or a mix of both. A 5V power supply is required when connecting more than one display. |
| [Output shift register](/devices/output-shift-register/) |   6   | Six _chains_ of shift registers, 32 bits each (2x16 or 4x8 bit shift registers).                                                         |
| [Servo](/devices/servo/)                                 |  12   |                                                                                                                                          |
| [Stepper](/devices/stepper-motor)                        |  10   |                                                                                                                                          |

## Pinout

{{< pinout >}}

> [!NOTE]
> Pins D0 and D1 are not available for use, as they are reserved for USB serial communication.

## Additional resources

- [3D model](https://grabcad.com/library/arduino-mega-2560--1)
- [Official technical documentation](https://docs.arduino.cc/hardware/mega-2560/)
- [Pinout diagram (PDF)](pinout.pdf)
