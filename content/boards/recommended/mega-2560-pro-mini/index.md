---
title: Mega 2560 Pro Mini
description: Details on MobiFlight support for the Mega 2560 Pro Mini.
ogimage: card-images/boards/mega-2560-pro-mini.png
weight: 10
---

{{< buy-in-shop url="https://shop.mobiflight.com/product/arduino-mega-2560-pro-mini-usb-c" >}}

The Mega 2560 Pro Mini offers the same 70 IO pins as the [Arduino Mega 2560 Rev3](/boards/arduino-mega-2560),
but in a smaller package. If you need many IO pins, this is the recommended board to use.

> [!WARNING]
> Many lower-cost Mega 2560 Pro Mini boards, particularly those purchased from AliExpress, use the CH340G chip for serial communication to the PC. These chips are frequently counterfeit and require [additional driver installation](/guides/installing-drivers/).
>
> Purchasing a Mega 2560 Pro Mini [from the MobiFlight Shop](https://shop.mobiflight.com/product/arduino-mega-2560-pro-mini-usb-c) ensures you will get a board with genuine chips.

{{< cards >}}

{{< card title="Mega 2560 Pro Mini" subtitle="ATmega2560 microcontroller" image="card-images/boards/mega-2560-pro-mini.png" >}}

{{</ cards >}}

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

- [Buy from the MobiFlight shop and help support the project](https://shop.mobiflight.com/product/arduino-mega-2560-pro-mini-usb-c)
- [3D model](https://grabcad.com/library/arduino-mega-2560-pro-3)
- [Datasheet](https://www.enmindustry.de/WebRoot/Store31/Shops/88169453/5FFE/0DC7/1617/A559/78B1/0A0C/6D12/6D9F/Mega2650PRO-Datasheet.pdf)
- [Pinout diagram (PDF)](pinout.pdf)
