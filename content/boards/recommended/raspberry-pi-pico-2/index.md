---
title: Raspberry Pi Pico 2
description: Details on MobiFlight support for the Raspberry Pi Pico 2.
images: [card-images/boards/raspberry-pi-pico-2.png]
weight: 50
aliases:
  - /boards/unsupported/raspberry-pi-pico-2/
---

The Raspberry Pi Pico 2 is a compact board with a moderate number of IO pins. It is a popular choice in builds where space is at a premium. Both the **Pico 2** and **Pico 2 W** are supported, however the wireless capabilities of the Pico 2 W are not used by MobiFlight.

{{< cards >}}

{{< card title="Raspberry Pi Pico 2" subtitle="RP2350/RP2354 microcontroller" image="card-images/boards/raspberry-pi-pico.png" >}}

{{</ cards >}}

## Specifications

- 23 digital IO pins, 16 with PWM support.
- 3 analog inputs (can be used as digital IO pins).

> [!TIP]
> Unlike the [Raspberry Pi Pico 1](/boards/raspberry-pi-pico/), the Pico 2 uses +5V data signals and does not need level converters when working
> with devices like the [MAX7219 display driver](/devices/seven-segment-display).

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
