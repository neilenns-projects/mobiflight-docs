---
title: Pro Micro (16MHz)
description: Details on MobiFlight support for the Pro Micro (16MHz).
ogimage: card-images/boards/pro-micro.png
weight: 30
---

{{< buy-in-shop url="https://shop.mobiflight.com/product/arduino-pro-micro-usb-c" >}}

The Pro Micro (16MHz) is a compact board that trades a smaller size for fewer IO pins than the Arduino Mega boards. It is a great choice when space is at a premium.

{{< cards >}}

{{< card title="Pro Micro (16MHz)" subtitle="ATmega32U4 microcontroller" image="card-images/boards/pro-micro.png" >}}

{{</ cards >}}

> [!WARNING]
> Some lower-cost Pro Micro clones, particularly those purchased from AliExpress, are [8MHz 3.3V variants](/boards/unsupported/pro-micro-8mhz) which are not supported by MobiFlight. Always check the product listing carefully to ensure you are ordering the 16MHz version.
>
> Purchasing a Pro Micro [from the MobiFlight Shop](https://shop.mobiflight.com/product/arduino-pro-micro-usb-c) ensures you will get a board running at 16Mhz.

## Specifications

- 12 digital IO pins, 5 with PWM support.
- 9 analog inputs (can be used as digital inputs).

| Device                                                   | Limit | Notes                                                                                                                                    |
| -------------------------------------------------------- | :---: | ---------------------------------------------------------------------------------------------------------------------------------------- |
| [Analog input](/devices/potentiometer/)                  |   9   |                                                                                                                                          |
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

## Additional resources

- [Buy from the MobiFlight shop and help support the project](https://shop.mobiflight.com/product/arduino-pro-micro-usb-c)
- [3D model](https://grabcad.com/library/arduino-pro-micro-1)
- [How to Revive a "Bricked" Pro Micro](https://learn.sparkfun.com/tutorials/pro-micro--fio-v3-hookup-guide/all#ts-revive)
- [Official technical documentation](https://www.sparkfun.com/pro-micro-5v-16mhz.html#documentation)
- [Pinout diagram (PDF)](pinout.pdf)
