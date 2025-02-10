---
title: Arduino Uno R3
description: Details on MobiFlight support for the Arduino Uno.
ogimage: card-images/boards/arduino-uno.png
weight: 20
---

The Arduino Uno R3 is an older design that doesn't offer many IO pins and has a large size.
Unless you already own one, we recommend purchasing a different board, either the
[Mega 2560 Pro Mini](/boards/mega-2560-pro-mini) if you need more IO pins (up to 70) or the
[Arduino Nano](/boards/recommended/arduino-nano) if space is at a premium.

{{< cards >}}

{{< card title="Arduino Uno" subtitle="ATmega328P microcontroller" image="card-images/boards/arduino-uno.png" >}}

{{</ cards >}}

## Specifications

- 14 digital IO pins, 6 with PWM support.
- 6 analog inputs (can be used as digital inputs).

| Device                                                   | Limit | Notes                                                                                                                                    |
| -------------------------------------------------------- | :---: | ---------------------------------------------------------------------------------------------------------------------------------------- |
| [Analog input](/devices/potentiometer/)                  |   6   |                                                                                                                                          |
| [Button](/devices/button-switch/)                        |  18   |                                                                                                                                          |
| [Digital Input Multiplexer](/devices/multiplexer/)       |   6   |                                                                                                                                          |
| [Encoder](/devices/encoder/)                             |   9   |                                                                                                                                          |
| [Input shift register](/devices/input-shift-register/)   |   6   | Six _chains_ of shift registers, 32 bits each (2x16 or 4x8 bit shift registers).                                                         |
| [LCD Display](/devices/lcd/)                             |   2   |                                                                                                                                          |
| [LED / Output](/devices/led/)                            |  18   |                                                                                                                                          |
| [LED 7-Segment](/devices/seven-segment-display/)         |   6   | 6 TM1637 modules, or 6 chains of MAX7219 modules, or a mix of both. A 5V power supply is required when connecting more than one display. |
| [Output shift register](/devices/output-shift-register/) |   6   | Six _chains_ of shift registers, 32 bits each (2x16 or 4x8 bit shift registers).                                                         |
| [Servo](/devices/servo/)                                 |   8   |                                                                                                                                          |
| [Stepper](/devices/stepper-motor)                        |   4   |                                                                                                                                          |

## Pinout

{{< pinout >}}

> [!NOTE]
> Pins D0 and D1 are not available for use, as they are reserved for USB serial communication.

## Additional resources

- [3D model](https://grabcad.com/library/arduino-uno-r3-ch340-1)
- [Official technical documentation](https://docs.arduino.cc/hardware/uno-rev3/)
- [Pinout diagram (PDF)](pinout.pdf)
