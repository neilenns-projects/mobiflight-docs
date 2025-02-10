---
title: Raspberry Pi Pico 1
description: Details on MobiFlight support for the Raspberry Pi Pico.
ogimage: card-images/boards/raspberry-pi-pico.png
weight: 40
---

The Raspberry Pi Pico 1 is a compact board with a moderate number of IO pins. It is a popular choice in builds where space is at a premium.

{{< cards >}}

{{< card title="Raspberry Pi Pico 1" subtitle="RP2040 microcontroller" image="card-images/boards/raspberry-pi-pico.png" >}}

{{</ cards >}}

> [!WARNING]
> MobiFlight only supports the Raspberry Pi Pico 1. The newer [Pico 2 board](/boards/unsupported/raspberry-pi-pico-2),
> with the RP2350 microcontroller, is not supported.

## Specifications

- 23 digital IO pins, 16 with PWM support.
- 3 analog inputs (can be used as digital IO pins).

> [!WARNING]
> The Raspberry Pi Pico 1 uses 3.3V for its digital signals. Certain output devices, including the MAX7219 7-segment LED driver chip and all LCDs, require 5V digital signals. If you plan to use those devices with the Pico, you will need to add a level shifter to your build.

| Device                                                   | Limit | Notes                                                                                                                                    |
| -------------------------------------------------------- | :---: | ---------------------------------------------------------------------------------------------------------------------------------------- |
| [Analog input](/devices/potentiometer/)                  |   3   |                                                                                                                                          |
| [Button](/devices/button-switch/)                        |  26   |                                                                                                                                          |
| [Digital Input Multiplexer](/devices/multiplexer/)       |   6   |                                                                                                                                          |
| [Encoder](/devices/encoder/)                             |  13   |                                                                                                                                          |
| [Input shift register](/devices/input-shift-register/)   |   6   | Six _chains_ of shift registers, 32 bits each (2x16 or 4x8 bit shift registers).                                                         |
| [LCD Display](/devices/lcd/)                             |   2   |                                                                                                                                          |
| [LED / Output](/devices/led/)                            |  26   |                                                                                                                                          |
| [LED 7-Segment](/devices/seven-segment-display/)         |   6   | 6 TM1637 modules, or 6 chains of MAX7219 modules, or a mix of both. A 5V power supply is required when connecting more than one display. |
| [Output shift register](/devices/output-shift-register/) |   6   | Six _chains_ of shift registers, 32 bits each (2x16 or 4x8 bit shift registers).                                                         |
| [Servo](/devices/servo/)                                 |   8   |                                                                                                                                          |
| [Stepper](/devices/stepper-motor)                        |   6   |                                                                                                                                          |

## Pinout

{{< pinout >}}

## Additional resources

- [3D model](https://datasheets.raspberrypi.com/pico/Pico-R3-step.zip)
- [Official technical documentation](https://www.raspberrypi.com/documentation/microcontrollers/pico-series.html#pico-1-technical-specification)
- [Pinout diagram (PDF)](pinout.pdf)
